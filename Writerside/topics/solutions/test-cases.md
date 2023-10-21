# The Test Case problem

>"*How do I know how many cases I should test in order to actually achieve high quality? And how can I choose suitable values for each case?*"

## The Problem
There is a science to generating the right test cases for a test. 

All but the simplest methods need testing with a variety of important combinations of parameters and data. Calculating these combinations is not simple. 

Vizitest's [Equivalence Class Partitioning](equivalence-classes.md) employs an algorithmic approach to test case creation. Other test types use a mix of art and science.

When trying to manually code more rigorous Test Case solutions you will often find yourself ...

- considering Test Cases based on thinking rather than letting an algorithm do the work for you
- spending time debugging test code
- constructing arcane and hard-to-maintain Test Case Table lookup systems.
- creating too few important test cases, affecting quality
- writing too many test cases, some of which are unnecessary or redundant, that take time to code and maintain and so incur cost.

## The Solution
Vizitest is based on the concept of Test Types.

Each Test Type offers a different approach to creating tests. 

- Some are optimized for out-and-out quality. 
- Others are more pragmatic and aim for ease-of-use while aiming for best possible quality.

However, all of our Test Types offer two things that save significant amounts of time.

- Auto-generation of test cases.
- Auto-generation of test code.

Each Test Type is backed by its own algorithm to determine how to generate the right number of test cases with the right data for each one.

