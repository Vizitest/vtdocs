# Nested Args and using constructors
**Unit B-B60** / **Repo folder : B_B50_PersonSimple** 

## Prep
- Find and open the training code **B_B50_PersonSimple** you [cloned from GitHub](github-repo.md).
- In the Test Manager, duplicate the **Complex Args** Test Configuration and call it **Nested Args, Constructors**. 
- Open the new Test Configuration.

## Introduction
This unit demonstrates two things.

- How we can specify a different constructor when instantiating the class.
- Nested complex data types.

## Task

### Modify the selected constructor in the Instance
In the Instance component, modify the Representative Value.

1. Select the value.
2. You can see the available constructors as orange buttons. 
3. Hover over the available constructors until you see the one with three parameters (name, age, dob).
4. Click on it.
5. Set the values to 
   
You'll notice that the parameter list changes to give the three parameters. ```LocalDate dob``` is itself a complex data type, so when you click on it, it's parameters are available to input.

This nesting continues as long as there are complex data types to deal with.

### Generate and run test
The method should already be configured if you cloned the previous unit's Test Configuration. So, you're ready to generate the test cases and test code, then run your test.





