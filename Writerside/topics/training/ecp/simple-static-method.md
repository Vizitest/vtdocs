# Simple static method
**Unit B-B20** / **Repo folder : B_B20_WaterState** 

## Prep
- Find and open the training code **B_B20_WaterState** you [cloned from GitHub](github-repo.md).
- In the Test Manager, make sure you have [created a Test Configuration](test-config-add.md) called **Water State**.

## Introduction
A static method is the simplest thing we can test.

In the ```WaterState``` class you'll see a simple method for getting the state of water at a given temperature.

## Requirements
We'll start off with the requirements for this method, which returns a string for the state of water at a given temperature in Degrees Celsius.

There will be those who want to argue about exactly when water freezes or turns to steam, but for the sake of simplicity, let's assume it is at 0 and 100.

<img src="ec-definition.png" alt="ec definition" width="300"/>

**We have a method that expects a temperature of water to be input. It should return the state of the water as a string.**

- The input parameter should be a floating point value
- The method is expected to return ```solid``` if the temperature is ```<=0```
- The method is expected to return ```liquid``` if the temperature is ```>0``` and ```<100```
- The method is expected to return ```gas``` if the temperature is ```>=100```
- It should throw an exception if the temperature is below absolute zero, ```<273.15```

## Task
Build a test for the method ```getWaterState(double temperature)``` according to the following table. We won't bother with *boundary values*. We'll deal with them in the next unit.

### Inputs
| Equivalence Class Name | Representative Values   |
|------------------------|-------------------------|
| **Ice**                | ```-10```               |
| **Water**              | ```50```                |
| **Steam**              | ```150```               |
| **Invalid**            | ```-300```, ```"xxx"``` |

Note that **Ice**, **Water** and **Steam** are all [Valid Equivalence Classes](B-B45-valid-invalid.md). This means that they contain values that are considered to be values that should result in a valid result. **Invalid**, on the other hand, contains invalid Representative Values that represent invalid input data.

Note that we've chosen arbitrary Representative Values for each Equivalence Class. Any value would do. 

We also defined two Representative Values for **Ice**. This is actually unnecessary but we are including 

### Verification -> Expected Values
| Equivalence Class Name | Representative Values                |
|------------------------|--------------------------------------|
| **State output**       | ```solid```, ```liquid```, ```gas``` |

The Representative Values are the three possible values that can be returned. The only other possible return is an Exception, which is dealt with separately as you'll see below.

1. Define the necessary [Equivalence Classes and Representative Values](ec-r-value-settings.md) for the Inputs as per the above Inputs table.
2. Do the same for the **Verification -> Expected Values** as shown in the per the **Verification -> Expected Values** table above.
3. Our method throws an exception if an invalid temperature is provided. We need to define this in the Verification -> Exceptions section. Hover over the Exception header bar and press **+**. You can rename it if you like. Leave it set to the general exception **Exception**.

Your configured test should now look like this.

[TODO - screenshot]


### Generate and run tests
1. Generate the test cases from the [Test Case Table](test-case-table.md) and set the Verifications as explained there. Not setting the Verification correctly will result in a warning, and you'll not be able to generate the test code.
2. [Generate the test code](codegen.md).
3. [Run the test](run-test.md).

Your test should pass. 

The eagle-eyed reader might have noticed there is actually a coding error that doesn't precisely meet the requirements. We'll deal with this in the next lesson.