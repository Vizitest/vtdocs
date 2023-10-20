# The Test Case Table
The Test Case Table shows your auto-generated test cases.

Initially, the table will be empty. When you have finished configuring your instance and method components, you can instruct Vizitest to generate your test cases by pressing the **Generate Test Cases** button.

Once this is completed, the table will show the test cases, one test case per column.

[TODO - screenshot]

Vizitest uses the "Pairwise Combination" algorithm to choose Instance and Input parameter values.

## Positive and negative test cases
At the top of each column you will see whether a test cases is 

- Positive - all the Representative values from Instance and Input parameters belong to valid Equivalence Classes
- Negative - one or more of the Representative values from Instance and Input parameters belong to invalid Equivalence Classes

This has two purposes

- It is a very useful visual indicator when you match Verifications (see below).
- It is used to control the assertion within the test code itself.

## Input parameters
For each auto-generated test cases, Vizitest chooses a single Representative Value to use. You can see which one was selected as it will show the value. All other cells in the test case column will be empty.

Although you can change the selected parameter by clicking on another value, you should be careful doing so. Vizitest's algorithm purposefully chooses these values.

You might want to add your own manual test cases, which is described [below](test-case-table.md#adding-a-manual-test-case).

## Matching Verifications to Inputs
You will not be able to generate your test code until all Verifications have been specified by you.

For each test case, selected the expected Verification by clicking in the Verification cell and choosing a value. You will choose the value based on the Input values. 

## Adding a manual test case
You do not actually need to use **Generate Test Cases** at all if you want to do everything manually by adding test cases yourself.

Alternatively, you might want to add a specific or important test case just to be sure it is being considered.

Press the **Add Test Case** button and a new column will be added to the test case table.

You should then ensure that all Instance and Method inputs have values selected by clicking in the appropriate cell.

You would then set the expected Verification to match.


## Editing test case header and other labels
You can change the test case title (Positive N to anything else) by clicking the label. You do not need to do this unless you want specific labelling in your test runner output or the test code comments.

You can also add the following information by clicking on the down arrow next to the title.

- Description - this is used for [TODO]
- Code comment - [TODO]
- Link  - [TODO]


## Removing test cases
There are two ways to remove test cases.

- Remove a single test case by pressing the trash icon.
- Remove all test cases by pressing the **Remove All Test Cases** button.

## Generating test code
The final step is to generate your actual test code. [Click here](codegen.md) to read about it.