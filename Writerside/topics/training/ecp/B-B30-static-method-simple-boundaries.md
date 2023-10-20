# Boundary values
**Unit B-B30** / **Repo folder : B_B20_WaterState** 

## Prep
- Find and open the training code **B_B20_WaterState** you [cloned from GitHub](github-repo.md).
- In the Test Manager, [create a Test Configuration](test-config-add.md) called **Water State Boundaries**. You can clone the **Water State** configuration we created in the previous unit.
- Open the new Test Configuration.

## Introduction
Boundary Values Analysis is an important concept in testing. This is explained in [Boundary Value Analysis](theory-ecs.md#boundary-value-analysis).

## Task

### Add Representative Values for Boundaries
Here's a table of Equivalence Classes and their Representative Values.

The reasons for choosing these values is explained in [Boundary Value Analysis](theory-ecs.md#boundary-value-analysis). The boundary values are shown in bold.

| Equivalence Class Name | Representative Value                              |
|------------------------|---------------------------------------------------|
| **Ice**                | ```-10```, **```-273.15```, ```-0.1```, ```0```** |
| **Water**              | ```50```, **```0.1```, ```99.9```**               |
| **Steam**              | ```150```, **```100```, ```100.1```**             |
| **Invalid**            | ```"xxx"```, ```-300```, **```-273.16```**        |

1. Add the boundary values to the respective Equivalence Class's Representative Values by [adding new Representative values](ec-r-value-settings.md#adding-a-representative-value). 
2. Our method throws an exception if an invalid temperature is provided. We need to define this in the Verification -> Exceptions section. Hover over the Exception header bar and press **+**. You can rename it if you like. Leave the general exception **Exception** default.
 

[TODO - check what happens with "XXX" R-value]

Your Method component should look like this.

[TODO - screenshot]

### Generate and run test
1. Generate the test cases from the [Test Case Table](test-case-table.md) and set the Verifications as explained there.
2. [Generate the test code](codegen.md).
3. [Run the test](run-test.md). **You should see that the test case fails due to one of the test cases failing**.

[TODO : screenshot]

### Correct the error
This error nicely illustrates one of the major benefits of the [Black Box Testing](black-box-testing.md) approach. 

We detected an issues without having needed to look at the ````getWaterState(double temperature)``` code implementation as we defined our test based solely on the requirements (see [previous unit](simple-static-method.md)).

We would now diplomatically inform the developer that there is an issue with the code. The developer would see that the following code snippet ...

```
if(temperature <= -273.15) {
    // There's a deliberate mismatch here between the requirements
    // It should be < -273.15, not <=
    // We'll use this to show a failed test
    throw new Exception("Temperature is below absolute zero");
}
```

... has an error with respect to the requirements. Specifically ```<= -273.15``` should be ```< -273.15```. A small but potentially significant error if this method was mission-critical.

Correct the code to ```if(temperature < -273.15) {``` and recompile.


### Re-run the test
When you re-run the test, it should now pass.

Hopefully we've managed to explain one of the major benefits of requirements based (black box) testing.

