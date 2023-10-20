# Black and White Box Testing
Vizitest is a Black Box Testing tool. It's also a White Box Testing tool.

You don't really need to know this to use Vizitest, but it's worth explaining why Black Box Testing is (in most cases) such a powerful approach and why much of Vizitest's functionality is black box oriented.

## White Box Testing
White box testing requires a developer to examine code before deciding on how to write the test. It therefore requires an in-depth knowledge of how the software is implemented. The developer then defines test cases that cover as much code as possible. Another way of putting this is - it is what black box testing and TDD is **not**.

All white box testing techniques are tightly coupled to the implementation. The author of the code under test usually implements the white box tests.

White box testing techniques usually focus on code coverage, taking into account statements, decisions/branches, condition testing or path testing.

In this whole process the specification/requirements do not necessarily play a role. White box testing tries to maximize the amount of code that is tested, but it doesn't necessarily validate if the tested code meets the actual requirements definition.

Furthermore, the tight coupling between code and white box tests causes tests to be fragile. Fragile tests tend to cause false positives when refactoring code.

There are cases where you really do want to white box test, but in most cases black box tests are better for quality.

## Black Box Testing
Black Box Testing get its name from the way it views the software as a black box with inputs and an output. A tester need have no knowledge of how the code is written inside the box.

The test is derived solely from the specification/requirements, which is why black box testing is also called specification testing. It forces the tester to concentrate on what the software does, not how it does it.

Because black box testing techniques require no knowledge of the systems implementation, testing and implementation can be done by separate people. In some cases the tester doesn't even have to have programming knowledge.

The most widespread black box testing techniques are equivalence class partitioning, boundary value analysis, state transition tables and decision table testing.

With black box testing we don’t know if all code is tested, but we can make sure, that it absolutely meets the requirements.

## Which is better?
It’s a case of “different horses for different courses”. There are some cases where you should use white box testing. It is a good technique for things that are prone to security issues as well as critical areas of the code that you feel need an extra level of testing.

But we would strongly suggest you use black box testing wherever you can. For most application types, this means “95% of the time”.

Some of the advantages of black box testing are :

- The developer can share or even shift the responsibility of requirements specification to other people such as POs, QA Engineers and Domain Experts.
- If you are interested in adopting Test Driven Design or TDD then you are black box testing by definition.
- Especially using tools like Vizitest, the developer can spend more time writing functional code and less time writing tests.
- You may not necessarily get perfect code coverage (and code coverage is very overrate, but that's another story) but you will get better quality.
- You will be a lot more productive and efficient in your ability to write quality tests across an entire application.

## What's Vizitest's role in all this?
Vizitest is fundamentally a Black Box Testing tool. It is always focused on the requirements rather than the implementation.

This does not mean that you can't use it for White Box Testing. The only difference is that you create your Test Configurations by looking at the implementation rather than the requirements.

We believe that in most (not all) circumstances, it is much more important to know that the Method Under Test meets the expected requirements than it is to know you have 100% code coverage.

One of the major benefits of Vizitest is that many tests can be easily configured by technical QA Engineers and nt just Software Engineers. This reduces the burden on Engineers and empowers QA teams.

Another benefit is the future readability of the test. Because everything is represented visually, anyone on the Product Team is able to understand the test without having to decipher hand-coded tests. 

