# The Test Case problem

>*"How on earth do I know what data to test with and what combinations of parameters I should test with in order to write a high quality test?*

## The Problem
There is a science to generating the right test cases for a test. 

All but the simplest methods need testing with all important combinations of parameters and data. Calculating this is tough. 

In the case of Equivalence Class Partitioning, it is a science. In the case of other test types, it is a mix of art and science. The possible impact of poorly designed test case :

- You may end up with too few test cases and you affect quality
- Or too many test cases, some of which are unnecessary and redundant and incur time and cost.

When trying to manually code more rigorous Test Case solutions you will often find yourself ...
- thinking about Test Cases based on thinking rather than letting an algorithm do the work for you
- spending time debugging the test code, let alone the functional code.
- constructing arcane and hard-to-maintain Test Case Table lookup systems.
- creating too few test cases, affecting quality
- creating too many test cases, incurring time and cost penalties.

## The Solution
Vizitest is based on the concept of Test Types.

Each Test Type offers a different approach to creating tests. 

- Some are optimized for out-and-out quality. 
- Others are more pragmatic and aim for ease-of-use while aiming for best possible quality.

However, all of our Test Types offer two things that save significant amounts of time.

- Auto-generation of test cases.
- Auto-generation of test code.

Each Test Type is backed by its own algorithm to determine how to generate the right number of test cases with the right data for each one.

