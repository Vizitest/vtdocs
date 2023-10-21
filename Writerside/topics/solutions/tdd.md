# Test Driven Development (TDD)

>*Test Driven Development seems like a great way to fully embrace unit and test integration. But adopting it feels very daunting for novices!*

## The Problem
It's not so much a problem as an opportunity.

TDD is indeed a great way of embracing testing. All TDD really states is that you write a test before you write the functional implementation. [Wikipedia](https://en.wikipedia.org/wiki/Test-driven_development) puts it like this.

1. **Add a test** - the adding of a new feature begins by writing a test that passes if the feature's specifications are met. The developer can discover these specifications by asking about use cases and user stories. A key benefit of test-driven development is that it makes the developer focus on requirements before writing code. This is in contrast with the usual practice, where unit tests are only written after the functional code.
2. **Run all tests** - the new test should fail for expected reasons. This shows that new code is actually needed for the desired feature. It validates that the test harness is working correctly. It rules out the possibility that the new test is flawed and will always pass.
3. **Write the simplest code that passes the new test** - inelegant, prototype code is acceptable, as long as it passes the test. The code will be honed anyway in Step 5. No code should be added beyond the tested functionality.
4. **All tests should now pass** - if any fail, the new code must be revised until they pass. This ensures the new code meets the test requirements and does not break existing features.
5. **Refactor as needed, using tests after each refactor to ensure that functionality is preserved** - code is refactored for readability and maintainability. In particular, hard-coded test data should be removed. Running the test suite after each refactor helps ensure that no existing functionality is broken.

**Repeat**
The cycle above is repeated for each new piece of functionality. Tests should be small and incremental, and commits made often. That way, if new code fails some tests, the programmer can simply undo or revert rather than debug excessively. When using external libraries, it is important not to write tests that are so small as to effectively test merely the library itself,[4] unless there is some reason to believe that the library is buggy or not feature-rich enough to serve all the needs of the software under development.

### So where's the problem
There isn't a problem, per se, but there are a couple of important considerations.

- How do I create a rigorous set of test cases given that test cases are critical to quality.
- Developers need a high degree of self-discipline to create the tests first without succumbing to the temptation of writing the functional implementation first.
  
## The solution
Vizitest fully support TDD and is a great way to implement it.

- TDD requires Black Box Testing techniques, a real Vizitest strength, as developers have to focus on the requirements first.
- Vizitest Test Configurations are visual, consistent and easy to understand without having to read code to infer intent.
- QA Engineers can work together with developers on test case creation, ensuring that the requirements come first and allowing the  developer to focus on the functional implementation.
- Writing great tests means using the right input data and then generating the right test cases. Vizitest is a major help with [Test Case Creation](test-cases.md).
- Vizitest generates highly consistent, best-practice test code that rarely required any debugging.

### Method signature
To use Vizitest for TDD, the only part of the functional code you need to write before configuring the test is the method signature. This does not materially violate TDD principles.

Once done, you can configure the test and run it. With no actual code, the test will fail, as expected. 

You can then start to add progressively more [Equivalence Classes and Representative Values](ec-r-value-settings.md) and implement the functional code.
