# The Code Coverage problem

> "*I'm so happy that I now get 90% code coverage. Why do I still have quality issues?*"  

## The Problem
There are 2 main approaches to testing:

- **Black Box Testing**: validates that the software does what it's supposed to according to the requirements.
- **White Box Testing**: reveals programming errors, side effects or detect security issues by inspecting the functional code implementation.

Most tests written with code coverage in mind examine the functional implementation as opposed to ensuring the requirements have been met. So, having even 100% coverage does not ensure quality.

In summary, the drawbacks of White Box Testing and a pure focus on coverage are

- focusing on the code and not on the requirements may show 100% coverage but if the requirements are not met, your code is still deficient.
- If the requirements ever change, it is difficult to modify the tests as there is no connection between requirements and test. A requirements based (Black Box) testing approach will pick up on deficiencies without even looking at the implementation code.
- You may end up constructing complex hard-to-maintain table lookup systems
- creating too few test cases, affecting quality
- creating too many test cases, incurring time and cost penalties.

## The Solution

We're not saying that you should _not_ create white box tests, and there are indeed cases where you might choose them over black box tests.

But in most cases it is better for quality to focus on the requirements and therefore prefer a black box test. 

Vizitest has Black Box and Requirements Led Testing at its heart and makes the process very much easier. However, Vizitest handles White Box Tests without compromise.
