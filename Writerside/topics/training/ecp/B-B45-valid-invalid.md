# Valid and Invalid Equivalence Classes

This is an informational unit only.

It is important to understand the relevance of **valid** and **invalid** Equivalence Classes.

- Firstly, they are a visual aid to help you differentiate between Representative Values that are intentional designed to trigger failures or error conditions within your code.
- Secondly, and more importantly, they provide Vizitest with vital information that is used to determine whether a test case is **expected** to pass or fail.

<img src="invalid-valid-values.png" alt="valid and invalid values" width="900"/>

## Instances, Input and Verification Equivalence Classes

### Instance and Method Inputs
As mentioned above, you need to ensure that the validity status of an Equivalence Class is correctly set.

When you work with the Test Case Table, you will notice that the column headers are either **Positive** (green) or **Negative** (red). 

- A **Positive** (green) Test Case tells Vizitest to assert that a test case has a positive result. If **all** Test Case values are valid, then the Test Case will be positive.
- Conversely, a **Negative** (red) Test Case tells Vizitest to assert that a test case expects a negative result. If **one or more** selected values are invalid, then the Test case will be Negative.

If you set these incorrectly then your test will produce false positives or fals negatives.

### Method Output
Technically, the validity status of Equivalence Classes in the **Return Values** section of the Method component does not matter. Nevertheless, we recommend you set the status appropriately to help visually differentiate between valid and invalid Output values.

Sometimes it can be ambiguous whether to set them as valid or invalid, so try to choose an Equivalence Class label that helps users understand what its purpose is.
