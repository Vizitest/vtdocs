# Valid and Invalid Equivalence Classes
**Unit B-B45**

This is an information until only.

It is important to understand the relevance of **valid** and **invalid** Equivalence Classes.

- Firstly, they are a visual aid to help you differentiate between Representative Values that are intentional designed to trigger failures or error conditions within your code.
- Secondly, and more importantly, they provide Vizitest with vital information that is used to determine whether a test case is **expected** to pass or fail.

## Instances, Input and Verification Equivalence Classes

### Instance and Method Inputs
As mentioned above, you need to ensure that the validity status of an Equivalence Class is correctly set.

When you work with the Test Case Table, you will notice that the column headers are either **Positive** or **Negative**. 

[TODO - screenshot of top of TCT]

- A **Positive** test case tells Vizitest to assert that a test case has a positive result.
- Conversely, a **Negative** test tells Vizitest to assert that a test case has a negative result.

If you set these incorrectly then your tests will fail for the wrong reasons.

### Method Verification
Technically, the validity status of Equivalence Classes in the **Expected Values** section of the Method component does not matter. Nevertheless, we recommend you set the status appropriately to help visually differentiate between valid and invalid Verification conditions.

Sometimes it can be ambiguous whether to set them as valid or invalid, so try to choose an Equivalence Class label that helps users understand what its purpose is.
