# The Instance component - Part 2
**Repo folder** : [src/main/java/B_B40_WaterStateInstance/WaterStateInstance.java](github-repo.md)

## Prep
- Find and open the training code **B_B40_WaterStateInstance** you [cloned from GitHub](github-repo.md).
- In the Test Manager, [create a new Test Configuration](test-config-add.md) called **Water State Instance - 2**.
- Open the new Test Configuration.

## Introduction
In the [previous unit](B-B40-water-state-instance-1.md), we saw how to manually create an Instance Component.

However, if we add a non-static Method Component, Vizitest will automatically add the Instance Component if it is not already on the canvas. This is a better approach as it requires less work.

## Task

### Add a Method component

1. [Add the ```getWaterState()``` Method](method-component.md) to the canvas **but make sure you use the one from the ```WaterStateInstance``` class and not ```WaterState```**. You'll see ```WaterStateInstance``` has been added as an Instance Component.

### Instance Component
We now want to instantiate the **Instance Component** with some Representative Values.

1. To the **Valid Values** Equivalence Class, add three Representative Values ```-50```, ```50```, ```150```.
2. To the **Invalid Values** Equivalence Class, add one Representative Value ```-300```.

<img src="instance-completed.png" alt="empty instance" width="500"/>

### Method Component
1. In the Input section you'll see that there are no parameters for the method. This is because, unlike the [previous example](B-B30-static-method-simple-boundaries.md), we initialize using the Instance Component and not a method argument Input.
2. We do need to add Representative Values in Output -> Return Values, however. 
3. In the **Output -> Return Values** section, add the following values to the **Valid Values** Equivalence Class : ```solid```, ```liquid```, and ```gas```.
4. And add the ```invalid temperature``` to the **Invalid Values** Equivalence Class.

You could optionally add Boundary Values as we did in the [earlier lesson](B-B30-static-method-simple-boundaries.md).

The Instance and Method components are now fully configured. Your test Configuration should now look like this.

<img src="instance-waterstateinstance-configured.png" alt="water state instance configured" width="500"/>

### Generate Test Cases and Test Code
1. Generate the test cases from the [Test Case Table](test-case-table.md) and set the Outputs as explained there. You can add Test Cases manually or automatically.
2. [Generate the test code](codegen.md).
3. [Run the test](run-test.md).

Your test should pass.
