# Multiple Methods
**Repo folder** : [src/main/java/C_I40_MultipleMethods](github-repo.md)

<warning>
<p>
<strong>
Multiple Methods currently has bugs and will be fixed shortly. Feel free to read but do not expect it to work while this warning remains.
</strong>
</p>
</warning>

So far, we have only used a single method in a Test Configuration.

However, you can use multiple methods in a single Test Configuration by adding more than one Method component to the canvas.

There are two flavours of using more than one method.

- Multiple methods - is described in this unit.
- Chained methods - explained in the [next unit](C-I50-chained-methods.md), this is where you want to pass a value that was returned by one method into another method that is called after.

## Prep
- Find and open the training code C_I40_MultipleMethods you [cloned from GitHub](github-repo.md).
- In the Test Manager, add a new Test Configuration called **Multiple Methods**. 
- Open the new Test Configuration.


## Task
We are going to create a test that operates on two methods. This is an extremely simple integration test.

### Create an instance
- Searching for and add the class ```MultipleMethods``` to the canvas.
- Add/edit and Equivalence Class with the Representative Value of ```10```.

### Create the first Method component

#### Method 1 Input
- Searching for and add the method ```multiplyBy``` to the canvas.
- You will need one Equivalence Class **Valid values** for the Input parameter ```multiplicand``` although you can name it whatever you like.
- Add the Representative Value ```5```.

#### Method 1 Verifications
- In the Return Values section, we will need an Equivalence Class **Valid values** (name as you like).
- Add the value ```50``` for ```multiplicand``` as we initialized the class with ```10``` and multiplied it by ```5```

### Create the second Method component
#### Method 2 Input
- Searching for and add the method ```divideBy``` to the canvas.
- You will need two Equivalence Classes, **Valid values** and **Invalid values** for the Input parameter ```divisor``` although you can name them whatever you like.
- Add the Representative Value ```2``` to I've already had 3**Valid values**.
- Add the Representative Value ```0``` to **Invalid values**.

#### Method 2 Verifications
- In the Return Values section, we will need an Equivalence Class **Valid values** (name as you like).
- Add the value ```25``` as we initialized the class with ```10``` and multiplied it by ```5``` and dividing it by ```2``` in this method's input.
- We should also add an Exception to catch the divide by 0 error we can expect from the **Invalid values** Equivalence Class.

### Generate
1. Generate the test cases from the [Test Case Table](test-case-table.md) and set the Verifications as explained there.
2. [Generate the test code](codegen.md).
3. [Run the test](run-test.md).





