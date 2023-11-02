# Boundary values
**Repo folder** : [src/main/java/B_B20_WaterState/WaterState.java](github-repo.md)

## Prep
- Find and open the training code.
- In the Test Manager, [create a Test Configuration](test-config-add.md) called **Water State with Boundaries**
  - by cloning the **Water State** configuration we created in the [previous unit](simple-static-method.md)
  - or creating a new one from scratch for more practice.
- Open the Test Configuration.

## Introduction
Boundary Values Analysis is an important concept in testing. This is explained in [Boundary Value Analysis](theory-ecs.md#boundary-value-analysis).

## Task

### Add Representative Values for Boundaries
Here's a table of Equivalence Classes and their Representative Values.

The reasons for choosing these values is explained in [Boundary Value Analysis](theory-ecs.md#boundary-value-analysis). The boundary values are shown in bold.

| Equivalence Class Name | Representative Value                 |
|------------------------|--------------------------------------|
| **Ice**                | ```-10```, **```-273.15```, ```-0.1```, ```0```** |
| **Water**              | ```50```, **```0.1```, ```99.9```**  |
| **Steam**              | ```150```, **```100```, ```100.1```** |
| **Invalid**            | ```-300```, **```-273.16```**        |

1. Add the boundary values to the respective Equivalence Class's Representative Values by [adding new Representative values](ec-r-value-settings.md#adding-a-representative-value). 
2. Our method throws an ```Exception``` if an invalid temperature is provided. We need to define this in the Output -> Exceptions section. Hover over the Exception header bar and press **+ Exception**.
 
<warning>
<p>
For the eagle eyed : we have made a deliberate error in the code. This will cause the test to fail. We will deal with this later in this unit. 
</p>
</warning>

Your Method component should look like this.

[TODO - screenshot]

### Generate Test Cases and Test Code
1. Generate the test cases from the [Test Case Table](test-case-table.md#automatic) and set the Outputs as [explained here](test-case-table.md#matching-outputs-to-inputs).
2. [Generate the test code](codegen.md).
3. [Run the test](run-test.md). **You should see that the test case fails due to one of the test cases failing**.

[TODO : screenshot]

### Correct the error
This error nicely illustrates one of the major benefits of [Black Box Testing](black-box-testing.md). 

We detected an issues without having needed to look at the ````getWaterState(double temperature)``` code implementation as we defined our test based solely on the [requirements](simple-static-method.md#requirements).

We would now inform the developer that there is an issue with the code. The developer would see that the following code snippet ...

```
if(temperature <= -273.15) {
    // There's a deliberate mismatch here between the requirements
    // It should be < -273.15, not <=
    // We'll use this to show a failed test
    throw new Exception("Temperature is below absolute zero");
}
```

... has an error with respect to the requirements. Specifically ```<= -273.15``` should be ```< -273.15```. A small, but potentially significant, error if this method was mission-critical.

Correct the code to ```if(temperature < -273.15) {``` and recompile.

When you re-run the test in the IDE, it should now pass.


