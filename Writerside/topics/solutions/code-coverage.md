# The Code Coverage problem

> *"I'm so happy that I now get 90% code coverage. So, why do I still have quality issues?" * 

## The Problem
There are 2 main approaches to testing:

- **Black Box Testing**: validates that the software does what it's supposed to according to the requirement.
- **White Box Testing**: reveals programming errors, side effects or detect security issues in within the code by inspecting the functional code implementation.

Both approaches have their place, but it is surprising how many people care so much about code coverage when it is absolutely no guarantee that all the requirements are met and the customer is satisfied.

More often than not, tests written with code coverage in mind examine the functional implementation as opposed to ensuring the requirements have been met. Even having 100% coverage does not ensure this.

In summary, the drawbacks of White Box Testing and a blind focus on coverage are

- focusing on the code and not on the requirements may show 100% coverage but if the requirements are not met, your code is still deficient.
- If the requirements ever change, it is difficult to modify the tests as there is no connection between requirements and test. A requirements based (Black Box) testing approach will pick up on this without changing or even having to look at the code.
- You may well end up making coding errors that take time to fix [HANNES ????]
- You may end up constructing complex hard-to-maintain table lookup systems
- creating too few test cases, affecting quality
- creating too many test cases, incurring time and cost penalties.

## The Solution

We're not saying that you should not create white box tests and there are cases where you might choose this in preference to a black box test.

But in most cases you should value the focus on the customer's requirements more and prefer a black box test. 

You can still write a white box test when you want to, but you can limit such tests to those cases where a white box test is well suited. This can be handled with Vizitest or a handwritten test.

Vizitest has Black Box and Requirements Led Testing at its heart and makes the process very much easier.
