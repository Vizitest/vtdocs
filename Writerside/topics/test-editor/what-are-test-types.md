# Test Types
A Test Type is a UI driven way of generating test code based on specific best-practice algorithms.

For example, a unit test using the [Equivalence Class Partitioning](equivalence-classes.md) test type might look like this.

<img src="example-test-config.png" alt="test type example" width="700"/>

1. Handles the instantiation of the class ```CreditCheck``` by creating single valid Equivalence Class with three different representative values.
2. Test the method ```checkCredit``` by defining input values and then possible Return Values, Custom Assertions, Exceptions and Side Effects.
3. An auto-generated test case table that can be completed by you to determine the correct returned value for each generated input.

## Current and future test types

During Beta, we offer one of the most powerful test types, [Equivalence Class Partitioning](equivalence-classes.md).

We will then start adding many more test types, such as 

- [API Testing](api-testing.md)
- [Decision Flow Table](decision-flow-table.md)
- [Decision Flow Diagram](decision-flow-diagram.md)
- Decision table testing
- State transition testing
- Cause–effect graph
- Error guessing
- State transition testing
- Use case testing
- User story testing
- Business process testing
- Acceptance based testing
- Behavior driven testing

