# Creating and coding Custom Assertions
Custom Assertions allow you to handle your own assertion logic. 

## Creating
You specify the use of a Custom Assertion in the [Method component](method-component.md).

<img src="custom-assertion-add.png" alt="custom assertion" width="400px"/>

1. In the Custom Assertions section of the Verification column, hover over the title bar and press the **+** icon.
2. Select the dropdown, which will initially contain ```null```.
3. Press the **Add new** button. You will then see the following dialog.

[TODO - screenshot and instructions; not currently working]


## Coding
Once you have [generated the test code](codegen.md) from the [Test Case Table](test-case-table.md), you will find the Custom Assertion code snippet in the test code itself.

```
private static void assertMyCustomAssertion(AllTogether instance, CreditReturnStatus result, CustomMatcherIsApprovedTestData data) {
    // TODO implement Custom Assertion
    // please implement your own custom assertion here
    // you can find the parameters defined for your custom matcher under data.<name>CustomMatcher
    // assertEquals(data.<name>CustomMatcher, result);
    throw new UnsupportedOperationException();
}
```

You should replace with internal boilerplate code with your own assertion logic. They important thing is that call ```assertEquals()``` (or other assert method) so the test runner can interpret the test outcome.

### Custom Assertion method arguments
The Custom Assertion method will always have at least one argument but may have up to three.

[TODO - Daniel please check all this below VERY CAREFULLY]

#### The ```data``` argument
This is always present. It has the rather lengthy and not too nicely named type of ```CustomMatcherCustomAssertionNameTestData``` where **CustomAssertionName** is the name you specified when defining the Custom Assertion in the Method component.

Its properties are the parameter values that you defined when adding the Custom Assertion.

#### The ```result``` argument
This will be present if the method under test has any return type other than ```void```. 

It contains the value that the method under test returned when being invoked with the test case data.

#### The ```instance``` argument
This will be present if the method under test is not static. It contains a reference to the Instance that the method belongs to.

