# The Instance component - Part 1
**Repo folder** : [src/main/java/B_B40_WaterStateInstance/WaterStateInstance.java](github-repo.md)

## Prep
- Find and open the training code **B_B40_WaterStateInstance** you [cloned from GitHub](github-repo.md).
- In the Test Manager, [create a new Test Configuration](test-config-add.md) called **Water State Instance - 1**. 
- Open the new Test Configuration.

## Introduction
Instance Components are used when you want to instantiate an object that should be referenced by a method later on.

We are only going to show how to create an Instance Component and set its Representative Value. We will see how the Instance Component can be automatically created in [Part 2](B-B40-water-state-instance-2.md).

If you look at the code in your IDE, you will see that we instantiate the class using a constructor that takes ```temperature``` as an argument.

## Task
Refer to the [Instance component](instance-component.md) documentation for general information and instructions.

1. Search for the ```WaterStateInstance``` class using the large **+** button in the top left of the canvas.
2. Add it to the canvas.
3. You will see that it has automatically added a **Valid Values** and an **Invalid Values** Equivalence Class.

<img src="instance-empty.png" alt="empty instance" width="500"/>

4. To the Valid Equivalence Class, add three Representative Values ```-50```, ```50```, ```150```.
5. To the Invalid Equivalence Class, add one Representative Value ```-300```.

<img src="instance-completed.png" alt="completed instance" width="500"/>

As you entered the values, you will notice that Vizitest has automatically chosen the (only) constructor to instantiate the object. You can find an example choosing from more than one available constructor in [this unit](B-B60-complex-args-nested.md).

<img src="instance-rvalue-selected.png" alt="empty istance" width="500"/>


