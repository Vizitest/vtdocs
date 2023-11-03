# Simple static method with Exception
**Repo folder** : [src/main/java/B_B20_WaterState/WaterState.java](github-repo.md) 

## Prep
- Find and open the training code.
- It's a good idea to be familiar with the [theory](theory-ecs.md) and [practice](practice-ecs.md) of Equivalence Classes.
- In the Test Manager, make sure you have [created the "Water State" Test Configuration](A-TM40-create-test.md).

## Introduction
A static method is the simplest thing we can test.

In the ```WaterState``` class you'll find a simple method ```public static String getWaterState(double temperature) throws Exception``` for getting a string representation of the state of water at a given temperature in Degrees Celsius.

## Requirements
There will be some who want to argue about exactly when water freezes or turns to steam. For the sake of simplicity, let's assume it's 0 and 100.

<img src="ec-definition.png" alt="ec definition" width="500"/>

**We have a method that expects a temperature of water to be input. It should return the state of the water as a string.**

- The input parameter should be a floating point value
- The method is expected to return ```solid``` if the temperature is ```<=0```
- The method is expected to return ```liquid``` if the temperature is ```>0``` and ```<100```
- The method is expected to return ```gas``` if the temperature is ```>=100```
- It should throw an exception if the temperature is below absolute zero, ```<273.15```

## Task
Build a test for the method ```getWaterState(double temperature)``` according to the following table. We won't bother with *boundary values*. We'll deal with them in the next unit.

### Add a Method Component
Use the [Search](search.md) to locate ```getWaterState()```. 

- Press the blue + icon in the top left of the canvas.
- Start typing ```getWaterState``` until you find the Method. **Note**: there are two methods with the same name. Be sure to select the one shown below.
- Click the + icon next to the method to add it to the canvas.

<img src="search-water-state.png" alt="search" width="600"/>

You should now see it added to the canvas. Note the highlighted **Input** and **Output** columns.

<img src="empty-method-component.png" alt="empty method component" width="900"/>

### Input
We are going to add Equivalence Classes and Representative values to pass to the method. The following table 

| Equivalence Class Name | Representative Values |
|------------------------|-----------------------|
| **Solid**              | ```-10```, ```-200``` |
| **Liquid**             | ```50```              |
| **Gas**                | ```150```             |
| **Invalid**            | ```-300```            |

Note that **Ice**, **Water** and **Steam** are all [Valid Equivalence Classes](B-B45-valid-invalid.md). This means that they should contain valid values within that Equivalence Class. 

**Invalid**, on the other hand, contains an invalid Representative Values (300).

Note that we've chosen arbitrary Representative Values for each Equivalence Class. Any valid value would do. 

We also defined two Representative Values for **Ice**, ```-10``` and ```-200```. This does not add value in this case,  but we're showing it just to show that it's possible.

### Output -> Return Values
| Equivalence Class Name | Representative Values                |
|------------------------|--------------------------------------|
| **Valid Values**       | ```solid```, ```liquid```, ```gas``` |

The Representative Values are the three possible values that can be returned. The only other possible return is an ```Exception```, which is dealt with separately as you'll see below.

### Method configuration

1. Define the necessary [Equivalence Classes and Representative Values](ec-r-value-settings.md) for the Inputs as shown in the Input table above. Rename the Equivalence Classes to match those in the table.
2. Do the same for the **Output -> Return Values** in the right column of the Method Component.
3. We do not need to create Representative Values for Invalid Values as our method handles errors by throwing an Exception.
4. Hover over the Exception header bar and press **+ Exception**. Leave it set to the general exception **Exception**. Note that you can click on **Exception** to choose another exception if it threw a custom exception.

Your configured Method Component should now look like this.

<img src="simple-static-method.png" alt="method configured" width="900"/>

### Generate Test Cases
1. [Add a manual Test Case](test-case-table.md#manual)  
  - set the Input to any valid Representative Value by clicking in the cell.
  - Click in the Output cell and select the Representative Value that you expect to be returned for the Input you specified.
  - You should see the Test Case labelled as **Test Case** in green. 
2. [Add another manual Test Case](test-case-table.md#manual)
   - set the Input to the **Invalid Value** ```-300.0``` by clicking in the cell.
   - Click in the Output cell and select **Exception** (which will be thrown for an invalid temperature value).
   - You should see the Test Case labelled as **Test Case 1** in red.
3. Optionally, add more Test Cases to match the screenshot below. 
4. [Rename your Test Cases](test-case-table.md#test-case-name-description-and-link) (by clicking in the Test Case name field) to match the screenshot below. Optional.

Your Test Case table should look approximately like this, depending on how many Test Cases you finally added.

<img src="simple-static-tct.png" alt="simple static test case table" width="900"/>

### Test Code
1. [Generate the test code](codegen.md) by pressing the **Generate Code** button. Make sure the test framework to the left of the button is set first.
2. [Run the test](run-test.md). Open the newly generated test code file in your IDE. The Path was indicated when you pressed the **Generate Code** button.
3. Run the test in your IDE.
4. The test runner should show your test passing. If it fails, then you should check your configuration and Input/Output values in the Test Cases. 
