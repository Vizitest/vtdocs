# The Test Case Table

The Test Case Table defines one or more distinct test cases, each of which runs against the Method Components in your test Configuration.

<tip>
    <p>
        When you add a Method Component, a <a href="test-case-table.md">Test Case Table</a> is automatically added. 
    </p>
</tip>

<img src="test-case-table-simple.png" alt="test case table" width="900"/>

- The first Test Case, **Ice**, uses the value ```-10.0``` and is expected to output the string value ```ice```.
- The third test Case, **Invalid**, use the input value ```-300.0``` and is expected to return the string value ```invalid temperature```.

## Creating Test Cases
There are two ways of creating Test Cases.

<img src="test-case-table-add-buttons.png" alt="test case table adding test cases" width="900"/>

### Manual
Add and define your own Test Case. This is a good way to control your Test Cases but requires you to build up a good and complete of Test Cases.

Press the **+Add Test Case** button to add a new Test Case column, then set the Inputs and Outputs as explained below.

### Automatic
Lets Vizitest generate an optimal set of Test Cases for you using a best practice algorithm (Pairwise Combination). You can remove or add Test Case afterwards.

This should not be used for methods that [TODO : Daniel???]

Press the **>> Generate Test Cases** button. Inputs will be automatically chosen but you will need to specify the expected Outputs as explained below.

## Positive and negative test cases
At the top of each column you will see whether a Test Case is expected to yield a positive or negative outcome.

<img src="test-case-table-col-headers.png" alt="test case table" width="900"/>

- **Positive** - automatically colored green if all the Representative values from Instance and Method Inputs as well as the Outputs belong to **valid** Equivalence Classes
- **Negative** - automatically colored red if one or more of the Representative values from Instance and Method Inputs as well as Outputs belong to an invalid Equivalence Class.

This has two purposes

- It is a very useful visual indicator when you match Verifications (see below).
- Vizitest uses this in the [Generated Test Code](codegen.md) to control the assertion itself. You do not need to do anything specifically.

## Input parameters

<img src="test-case-table-input.png" alt="test case table input" width="900"/>

For each auto-generated Test Case, shows the Representative Value to use. This can be edited and will show available values as defined in Instance or Method components.

The above screenshot shows the user having licked on the second Test Cases, You can see the value ```50.00``` has been selected.

If you Test Cases were automatically generated, these will be prefilled.

You would usually need all Input parameter cells to have values specified to be able to [Generate Test Code](codegen.md).


## Matching Outputs to Inputs

<img src="test-case-table-output.png" alt="test case table output" width="900"/>

The Output for each Test Case will need to be manually matched by you in order to be complete, ready for [Test Code Generation](codegen.md).

This is the case even if you generated Test Case automatically.


## Test Case metadata
You can change the test case title (Positive N to anything else) by clicking the label. You do not need to do this unless you want specific labelling in your test runner output or the test code comments.

<img src="test-case-table-extra.png" alt="test case table extra info" width="900"/>

You can also add the following information by clicking on the down arrow next to the title (circled).

- Description - Will appear when you hover on the Test Case title.
- Code comment - text that should be inserted into the generated test code.
- Link - a link to any external URL you may want to include as a reference. 


## Removing test cases
There are two ways to remove test cases.

- Remove a single test case by pressing the trash icon.
- Remove all test cases by pressing the **Remove All Test Cases** button.

<img src="test-case-table-remove.png" alt="delete test case" width="900"/>


## Generating test code
Once your Test Cases have been fully configured with Input and Output values, you are ready to [generate the test code](codegen.md).