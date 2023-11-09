# Practice
Please make sure you've read the [Theory page](theory-ecs.md). 

This defines the terms we are using, a requirements statement for our Method Under Test and explains how and why we use the values mentioned below.

## Requirements
As a reminder, we have the following requirements.

**We have a method that expects a temperature of water to be input. It will return the state of the water as a string.**

- The input parameter should be a floating point value
- The method is expected to return ```solid``` if the temperature is ```<=0```
- The method is expected to return ```liquid``` if the temperature is ```>0``` and ```<100```
- The method is expected to return ```gas``` if the temperature is ```>=100```
- It should throw an exception if the temperature is below absolute zero, ```<273.15```

## Equivalence Classes and Representative Values
We have the following Equivalence Classes. We have also included boundary values around the sensitive boundary values, for example ```-273.15```, ```0``` and ```100```.

| Equivalence Class Name | Representative Value                          |
|------------------------|-----------------------------------------------|
| **Ice**                | ```-273.15```, ```-10```, ```-0.5```, ```0``` |
| **Water**              | ```50```, ```+0.5```, ```99.5```              |
| **Steam**              | ```150```, ```100```, ```100.5```             |
| **Invalid**            | ```-300```, ```-273.16```, ```"xxx"```        |

## Definition in Vizitest
Having decided on the Equivalence Classes and Representative Values, we can implement these directly in Vizitest. The image below shows the use of Equivalence Classes within a Method Component. You can read how to [work with the Method component here](method-component.md). They are also used in the [Instance Component](instance-component.md).

### Configuration without boundary values
We are just configuring with one valid value in each Equivalence Class. 

<img src="ecs-no-boundaries.png" alt="ecs no boundaries" width="500"/>

### Configuration with boundary values
To be more thorough, we've also added the boundary values we showed in the table above.

<img src="ecs-with-boundaries.png" alt="ecs no boundaries" width="500"/>


>
>Note that next to each Equivalence Class there is either a green '✓' symbol or a red 'x' symbol. This has a specific and important purpose. 
>
>- '✓' indicates that the Equivalence Class contains **valid** Representative Values
>- 'x' indicates **invalid** Representative Values.
>
>You will specify this when adding the Equivalence Class in Vizitest. It is then used when the test cases and the test code is generated. You can toggle valid/invalid by clicking on the icon.


### Input parameters
In the above example, we can see ```static String getWaterState()``` component. This has a single input parameter ```double temperature```.

If your method takes multiple parameters, they will appear beneath one another in the Input column.

<img src="input-parameter.png" alt="input parameter" width="500"/>


### Output - Return Values
We also use the concept of Equivalence Classes to define possible return values. For this, there is a set of valid return values that we will name **Results**. It can contain Representative Values of ```solid```, ```liquid``` and ```gas```.

<img src="output-return-values.png" alt="return values" width="500"/>

If your method were to return a values or values that indicated an invalid response (```invalid``` for example), then you can choose whether to include this in the ***Results*** or create an invalid Equivalence Class with ```invalid``` as its Representative Value. Unlike the inputs, where it is important, for Verifications it is a visual aid.

### Output - Exceptions
If your method can throw an exception, then you should add the exception as a possible output. Hovering over the title bar will present the **+Exception button**.

<img src="output-exception.png" alt="return values" width="500"/>

This is explained in [this Simple Static Method training unit](simple-static-method.md).


## Test Case Table
The Test Case Table defines one or more distinct test cases, each of which runs against the Method Components in your test Configuration.

<img src="test-case-table-simple.png" alt="input parameter" width="700"/>

Refer to the [Test Case Table](test-case-table.md) page for full details. 

### Manual

### Automatic
Generating the [Test Case Table](test-case-table.md) is a key step and one that has the following major advantages.
[TODO - link to TCT when present]

- It ensures that an optimal number of test cases are automatically generated
- It saves a great deal of time having to think about what test cases you should create
- It eliminates the potential for coding errors in the tests themselves

Vizitest uses a special algorithm for this (Pairwise Combination). It's beyond the scope of this page to explain it, but let's just say this is the part that automatically generates the optimal number of test cases. It does not generate every imaginable combination, rather examines the Equivalence Classes and decides which ones are important.

We will soon add the option to generate all possible combinations. This has advantages but also disadvantages in that you can end up with a huge number of test cases. It generally would only make sense for certain mission-critical methods where it is worth the slowdown in speed.

[TODO - proper image for the TCT]

![](test-case-table.png)

You press Generate Test Cases and the test cases are then displayed in columns, one test case per column.

You then examine each test case and specify which Verification is expected for the given inputs.

## Automatic Test Code Generation
Once you have matched the Verifications to the inputs, you are ready to generate your test code. This is a one button press operation.

[TODO - need image with generate test code button]

Vizitest generates so-called parameterized tests, which makes your code both compact and readable. The test code is regular code and can be read, run and launched just like any other test you would write manually. 

[TODO correct image once codegen done]

![](codegen.png)

