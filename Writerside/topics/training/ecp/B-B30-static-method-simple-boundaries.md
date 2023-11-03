# Boundary values
**Repo folder** : [src/main/java/B_B20_WaterState/WaterState.java](github-repo.md)

## Prep
- Find and open the training code.
- In the Test Manager, [create a Test Configuration](test-config-add.md) called **Water State with Boundaries**
  - by cloning the **Water State** configuration we created in the [previous unit](simple-static-method.md)
  - or creating a new one from scratch for more practice.
- Open the Test Configuration.

## Introduction
Boundary Values Analysis is an important testing concept. We explain it in [Boundary Value Analysis](theory-ecs.md#boundary-value-analysis).

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
2. Our method throws an ```Exception``` if an invalid temperature is provided. We need to define this in the Output -> Exceptions section. Hover over the Exception header bar and press **+ Exception**. It should default to the general ```Exception```, which is correct.
 
<warning>
<p>
For the eagle eyed : we have made a deliberate error in the code. This will cause the test to fail. We will deal with this later in this unit. 
</p>
</warning>

Your Method component should look like this.

<img src="training-boundary.png" alt="method component with boundary values" width="900"/>


### Generate Test Cases and Test Code
1. Press the Generate Test Cases button. This is what you should see (although this shows the Output values set, which they won't be for you).

<img src="training-boundary-tct.png" alt="test case table" width="900"/>

2. **Note**: this generates quite a lot of Test Cases, so click and drag within the Test Cases area to scroll across.
3. Set the Output values to suit the auto-generated Input temperature.
4. [Generate the test code](codegen.md) then open it in your IDE.
5. [Run the test](run-test.md). **You should see that the Test Case fails due to one of the Test Cases failing**.

<img src="training-boundary-test-fail.png" alt="test case run failure" width="900"/>


### Correct the error
This error nicely illustrates one of the major benefits of [Black Box Testing](black-box-testing.md). 

We detected an issues without having needed to look at the ```getWaterState()``` code implementation as we defined our test based solely on the [requirements](simple-static-method.md#requirements).

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


