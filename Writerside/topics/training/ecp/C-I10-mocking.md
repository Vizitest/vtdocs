# Test Doubles - Mocking and Stubbing
**Repo folder** : [src/main/java/C_I10_Mocking](github-repo.md)

This unit assumes that you already familiar with stubbing, mocking and spies.

We will only deal with **Stubbing**, the most widely used technique within what is often and slightly misleadingly referred to as **Mocking**.

Once you understand this example, implementing mocking (as opposed to stubbing) should be obvious.


## Prep
- Find and open the training code.
- In the Test Manager, add a new Test Configuration called **Mocking and Stubbing**. 
- Open the new Test Configuration.

## Introduction
You might want to read the [Mocking and Stubbing page in the User Guide](mocking.md).

If a method has an external dependency, then in order for it to be a true unit test, that dependency will need to be mocked or stubbed.


## Example
Take a look at the following code that implements a method ```addUser()``` in a service for adding a user to a database.

You can find this code in ```src/main/java/C_I10_Mocking/service```.

```
public class UserService implements IUserService {

    private final IAddUserRepository addUserRepository;

    public UserService(IAddUserRepository addUserRepository) {
        this.addUserRepository = addUserRepository;
    }

    public boolean validateUser(String name, String age) {
        int numAge = Integer.parseInt(age);
        if(name.length() < 4) return false;
        if(numAge < 18 || numAge > 120) return false;
        return true;
    }

    public void addUser(String name, String age) throws Exception {
        if(!validateUser(name, age)) throw new Exception("Illegal argument somewhere or other");
        User user = new User(name, Integer.parseInt(age));
        user.setBio("No bio available");
        addUserRepository.execute(user);
    }

}
```

The problem is that ```addUserRepository.execute(user)``` is an external dependency and saves as user to the database. This would violate the unit test principles of **Fast** and **Isolated**.

To solve this, we will mock ```addUserRepository.execute()```.

## Vizitest solution
The way you address this in Vizitest currently is to create a User Method. We will soon be adding a UI based approach that avoids the need to code at all.

## Task

### Add an Instance component
We are going to accomplish the following : "When the UserService class is instantiated, we need to create a dummy method (stub) that simulates what ```addUserRepository``` would do in reality. This means it should return a User object, whose contents we can predict for the purposes of testing."

- Add an Instance component for the ```UserService``` class.
- We only need one Equivalence Class. Call it ```Mock addUserRepository```
- We just need one Representative Value for this, which will handle the mocking, so add one now.
- Select this newly added value and click on **+ User Method**.
- Enter **mockAddUserRepository** as the method name.
- Add three parameters ```String name```, ```int age```, ```String bio``` and press **Add**.
- Set these parameters to ```John Brook```, ```34``` and ```Composer of Baroque Music```.

You may be wondering how we actually handle the mocking itself. We will do this once we have generated the test code, which is explained at the bottom.

### Add the Method component
We can deal with the Method Under test ```addUser(String name, String age)```.

#### Inputs
Let's set up the method parameters' Equivalence Classes.

- For the **name** parameter
  - Add/edit a Representative Value to the  **Valid** Equivalence Class and set to **John Brook**
  - Add/edit a Representative Value to the  **Invalid** Equivalence Class and set to **JB**
- For the **age** parameter
  - Add/edit a Representative Value to the  **Valid** Equivalence Class and set to **34**
  - Add/edit a Representative Value to the  **Invalid** Equivalence Class and set to **10**

If you wanted to be thorough, you could also add [Boundary Values](B-B30-static-method-simple-boundaries.md) for these, but we haven't to keep things simple.


### Output
We should now set up the Return Values and Exceptions.

#### Return Values
The good news for us here is that ```addUser()``` is void, so we don't have to worry about these at all. It either works or it throws an exception, so let's handle that.

#### Exceptions
You can see that ```addUser()``` throws an exception if the validation fails.

In the Exceptions section, add an exception to the list and set to **Exception**, the general exception.

### Generate and run test
You can now generate the test cases, then the test code and finally run the test.

This test will fail as we haven't yet written the mocking code.

### Write the mocking code
If you open the generated test code, you will find the following auto-generated method.

```java
//region Factories
	private static IAddUserRepository mockAddUserRepository(String name, Integer age, String bio) {
		// TODO implement factory
		throw new UnsupportedOperationException();
	}
//endregion
```

You can now replace the method implementation as follows.

```
	private static IAddUserRepository mockAddUserRepository(String name, Integer age, String bio) {
    IAddUserRepository mockRepo = mock(IAddUserRepository.class);
    User expected = new User(name, age, bio);
    when(mockRepo.execute(any().thenReturn(expected)));
	}
```

We will soon be handling mocking configuration in the Vizitest UI, removing the need to write this code at all.
