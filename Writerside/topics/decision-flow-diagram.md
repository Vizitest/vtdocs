# Decision Flow Diagram

## AVAILABLE Q2 2024

## Overview

The **Decision Flow Diagram** is similar in concept to the [Decision Flow Table](decision-flow-table.md).

The screenshot below is a very rough mockup.

You specify a set of validation and execution tests in a flow diagram. This can be well suited to tests where there a branching rules that may be best represented in a diagrammatic form.

- You VALIDATE parameters in a dedicated section. Vizitest will handle the internal logic for you.
- The actual test logic is in the EXECUTE section.
- Branch conditions can be defined on the edges, including support for complex data types.


![](decision-flow-diagram-mockup.png)

## Advantages

- It is easy to set up.
- It is easy to read and understand in the future.
- It is well suited to methods where more complex branching logic is better represented in diagrammatic form.
- Vizitest will translate everything into a clear set of test cases and then into test code.
- You can examine the test cases and even add new ones in a [Test Case Table](test-case-table.md) should you want to, although this would not usually be necessary.

## Disadvantages

- It is not as rigorous as [Equivalence Class Partitioning](theory-ecs.md).
- Another test type may be better suited to the task (we will be constantly adding more tes types).

## Your thoughts and ideas
If you would like to contribute your ideas to this test type, please email support@vizitest.com. We are always happy to jump on Zoom calls to anyone who wants to discuss their ideas with us.