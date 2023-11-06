# Custom Assertions
**Unit C-I80** / **Repo folder : C_I80_CustomAssertions** 

## Prep
- Find and open the training code C_I80_CustomAssertions you [cloned from GitHub](github-repo.md).
- In the Test Manager, add a new Test Configuration **Custom Assertions**. 
- Open the new Test Configuration.

## Introduction
First refer to the User Guide page on [Creating and coding Custom Assertions](custom-assertions.md).

## Task
In the test Editor, create the following four Method Components and for each of the four available methods in the training code. For each one, create a Custom Assertion using the **Suggested User Method name** in the table below.

<warning>
<p style="color:white">TODO</p>
<p>
The information below is under review and may not be 100% accurate.
</p>
</warning>


| Method                       | Suggested User Method name | Generated method                                                                                      |
|------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------|
| ```multiplyByStaticVoid```   | StaticVoidCA               | ```private static void assertStaticVoidCA(User result, CustomMatcherStaticVoidCATestData data)```     |
| ```multiplyByStaticDouble``` | StaticDoubleCA             | ```private static void assertStaticDoubleCA(User result, CustomMatcherStaticDoubleCATestData data)``` |
| ```multiplyByVoid```         | VoidCA                     | ```private static void assertVoidCA(User result, CustomMatcherVoidCATestData data)```                 |
| ```multiplyByDouble```       | DoubleCA                   | ```private static void assertDoubleCA(User result, CustomMatcherDoubleCATestData data)```             |

You'll notice that, depending on whether the method is static/non-static or void/non-void, you will have a different number of arguments. The reason for this is [explained here](custom-assertions.md#custom-assertion-method-arguments).

### Code for the Customer Assertions

<warning>
<p>
TODO - code example coming soon.
</p>
</warning>

We are not actually doing anything here that couldn't be accomplished using the normal Verification -> Expected Values. But we do want to show how Custom Assertions work, so below is the code for each of our four examples.

#### ```private static void assertStaticDoubleCA(User result, CustomMatcherStaticDoubleCATestData data)```
This example will make its assertion based on **actual** values in ```result``` and the **expected** values in ```data```.

#### ```private static void assertVoidCA(User result, CustomMatcherVoidCATestData data)```

#### ```private static void assertDoubleCA(User result, CustomMatcherDoubleCATestData data)```


