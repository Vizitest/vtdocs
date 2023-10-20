# About Test Configurations
A Test Configuration defines one or more unit or integration tests using the Vizitest low-code user interface.

During the Beta, we offer one of the most powerful ways of generating tests, known as [Equivalence Class Partitioning](equivalence-classes.md).

We will add more [test Types](what-are-test-types.md) in the future.

:::info
All Test Configurations are stored in the ```.vizitest``` folder in the root of your codebase. The folder structure mirrors that of your Test Manager Groups. Each Test Configuration also has a folder with the configuration metadata stored a ```.tconfig``` and a ```.yaml``` file.

This is for informational purposes only. You shouldn't need to modify these yourself. 

It's also worth noting that all Vizitest metadata plays nicely with Git, so you can roll back using Git should you need to.
:::

## Unit vs. Integration Tests
Vizitest doesn't explicitly differentiate between unit and integration tests. Vizitest just allows you to configure tests which can then be thought of as 

- unit tests is you are testing a single method that is logically isolated in a system
- integration tests otherwise.

