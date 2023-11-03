# Multiple Test Configurations for the same Class

<warning>
<strong>
This unit is informational only but it contains important informaion to be aware of.
</strong>
</warning>

## Introduction
When you generate test code, it creates a test file in your project, like this.

<img src="training-project-tests.png" alt="project tests" width="400"/>

As you can see, a test Class is written to a package with the same Class name (+ Tests) as the main source Class.

In the above image, we are testing ```B_B20_WaterState/WaterState```.

### Problem
If you were to create another Test Configuration, containing Method or Instance components that belong to that Class, then when we generate the test code, teh test code file ```WaterStateTest``` would be overwritten.

### Solution
The way we handle this is to make a change to the Path field when we generate the test code.

When you press **Generate Code** in the Test Case Table, the following dialog appears.

<img src="training-multiple-tcs.png" alt="test code path" width="700"/>

The field contents will look something like

- /Users/johnbrook/dev/vizitest-training/src/test/java/B_B20_WaterState/WaterStateTest.java

All you need to do is to change the filename to be something unique, so for example.

- /Users/johnbrook/dev/vizitest-training/src/test/java/B_B20_WaterState/WaterStateTest_**second**.java

<tip>
We replace this approach with an improved dialog to make this a) clearer and b) persistent.
</tip>

