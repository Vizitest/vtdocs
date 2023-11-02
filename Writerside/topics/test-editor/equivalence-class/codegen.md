# Generating test code
Once you've completed the [Test Case Table](test-case-table.md), you're ready to generate the actual test code.


<img src="test-case-table-generate-code.png" alt="generate test code" width="900"/>

Before you press the **Generate Test Code** button, make sure a framework is selected. Currently, only JUnit is supported. 

The test code is designed to run under the test runner framework you selected. It can therefore run in your IDE or in any other workflow.

When you press it, Vizitest will ask you to specify the root path within your codebase where the test code should be generated. You would typically use the same path for all tests. [TODO - Daniel, is this correct?]

<img src="test-case-table-generate-code-dialog.png" alt="choose test code path" width="500"/>

## Running tests
[Click here](run-test.md) for details on running the generated test code.

