# Overview
** *Available in Q2 2024* **

Although the screenshot below is only a rough mockup, it should explain the concept well enough.

The idea is that you specify a sequence of rules and conditions with respect to a Method. 

- Each row condition is in sequence. If the condition evaluates to true, then it will either return the indicated value or it will - thrown an exception.
- If the condition evaluates to false, then the next row is evaluated, and so on.
- If none of the rows evaluated to true, the **OTHERWISE** row specifies what value to return, or what Exception to throw.
- If a cell is left empty, Vizitest will handle it for you.
- It will handle complex data types elegantly.

![](decision-flow-mockup.png)

## Advantages

- It is easy to set up.
- It is easy to read and understand in the future.
- Vizitest will translate the table into a clear set of test cases and then into test code.
- You can examine the test cases and even add new ones in a [Test Case Table](do-test-case-table.) should you want to, although this would not usually be necessary.

## Disadvantages

- It is not as rigorous as [Equivalence Class Partitioning](ec-theory.).
- Another test type may be better suited to the task (we will be constantly adding more tes types).

## Your thoughts and ideas
If you would like to contribute your ideas to this test type, please email support@vizitest.com. We are always happy to jump on Zoom calls to anyone who wants to discuss their ideas with us.