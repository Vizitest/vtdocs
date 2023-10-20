# Method Component

Please refer to the Equivalence Class [Theory](theory-ecs.md) and [Practice](practice-ecs.md) pages if you are not yet familiar with Equivalence Classes.

## 1. Add the Method
When you want to test a method, you use the Method component. To add a new one to the canvas

<img src="method-class-search.png" alt="Class method search" width="600"/>

- Click on the + icon as shown in the image above to open the search dialog.
- Enter the name of the method you want to add (you can filter using the dropdown).
- Press the + icon to add to the canvas.

You should now see a new component on the canvas.

<img src="method-component.png" alt="method component"/>

You will notice that the Method component has several sections, divided into Inputs and Verification.

Your final configuration will be used by the [Test Case Table](test-case-table.md).

## Inputs
The Input column will contain several sections, one for each method parameter. You should create at least one Equivalence Class for each parameter with at least one Representative Value in each Equivalence Class.

## Verification
This is where you define possible/expected outputs from the method. These are divided into the following sections.

- **Expected Values** - one or more Equivalence Classes (usually just one) with one Representative Value for each expected value you want to test against.
- **Exceptions** - if your method throws Exceptions, you will want to specify the Exception type. For each different Exception type you expect, add a new row by hovering on the Exception section header and pressing the + icon. You select the Exception type from the dropdown. If you select **Exception**, then it will handle all Exceptions including custom exceptions.
- **Custom Assertions** - If you want to write your own code to handle the assertion. For a detailed explanation on how to define and code the Custom Assertion, [click here](custom-assertions.md).
- **Side Effects** - if your method a) doesn't return a value that you can test against and b) mutates the object properties such then you can use Side Effects to test against the state of the object after the method has executed. Please refer to the [Side Effects page](side-effects.md) for a more detailed explanation.

## 2. Add Equivalence Class(es)
Currently, you need to add at least one Equivalence Class and one Representative Value, even if the constructor doesn't have any arguments. 

This is described in detail [on this page](ec-r-value-settings.md#adding-an-equivalence-class-to-an-instance).

## 3. Add Representative Values
Each Equivalence Class requires at least one Representative Value.

Adding a Representative Value is described in detail [on this page](ec-r-value-settings.md#adding-a-representative-value).

If there is only a default constructor or one without arguments, then you should still add one. Just go ahead and set it [TODO - how does this actually look in this case?]

The more Equivalence Classes and Representative Values you add, the more test cases you will end up with. So don't add unnecessary ones so the amount of Input/Verification matching does not become unnecessarily large. [TODO - Daniel, not completely happy with this statement and it may be wrong!!!]

[TODO - explain how the ECs are related to the TCT once the TCT is working]
