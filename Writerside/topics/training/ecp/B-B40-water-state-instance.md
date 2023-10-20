# The Instance component
**Unit B-B40** / **Repo folder : B_B40_WaterStateInstance** 

## Prep
- Find and open the training code **B_B20_WaterStateInstance** you [cloned from GitHub](github-repo.md).
- In the Test Manager, [create a new Test Configuration](test-config-add.md) called **Water State Instance**. 
- Open the new Test Configuration.

## Introduction
This unit is a variation on the [previous unit](B-B30-static-method-simple-boundaries.md).

In most cases, you will not be using static methods. So, you should create an Instance component first in order to associate the Method Under Test with its parent Instance.

Rather than using a static method, we have a class ```WaterStateInstance``` and set the temperature in its constructor.

We then get the water state using ```String getWaterState()```.

## Task

### Add an Instance component.
Refer to the [Instance component](instance-component.md) documentation for general information and instructions.

1. Search for the ```WaterStateInstance``` class using the large **+** button in the top left of the canvas.
2. Add it to the canvas.
3. You will see that it has automatically added a Valid and an Invalid Equivalence Class.
4. To the Valid Equivalence Class, add three Representative Values ```-50```, ```50```, ```150```.
5. To the Invalid Equivalence Class, add one Representative Value ```-300```.
6. You could optionally add Boundary Values as we did in the [earlier lesson](B-B30-static-method-simple-boundaries.md).

You will notice that Vizitest has automatically chosen the (only) constructor as the means of instantiating the object. We'll see an example of working with multiple constructors in the [next unit](B-B60-complex-args-nested.md).

[TODO : screenshot]

### Add a Method component
Now that we have defined the instance, we need to test the method by adding a Method component.

1. [Add the ```getWaterState()``` Method](method-component.md) to the canvas **but make sure you use the one from the WaterStateInstance class and not WaterState**.
2. In the Input section you'll see that there are no parameters for the method. This is because, unlike the [previous example](B-B30-static-method-simple-boundaries.md), we initialized using the constructor and not method arguments.
3. We do need to add an Equivalence Class for the Verification => Expected Values, however. Add one and name it **Method output**.
4. In the **Verification -> Expected Values** section, you should configure one Equivalence Class with three Representative Values - ```solid```, ```liquid```, and ```gas```.

The Instance component now has all the interesting details. Your test Configuration should now look like this.

[TODO : screenshot]


### Generate
1. Generate the test cases from the [Test Case Table](test-case-table.md) and set the Verifications as explained there.
2. [Generate the test code](codegen.md).
3[Run the test](run-test.md).

Your test should pass.
