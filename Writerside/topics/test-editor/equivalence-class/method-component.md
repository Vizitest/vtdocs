# Method Component

Please refer to the Equivalence Class [Theory](theory-ecs.md) and [Practice](practice-ecs.md) pages if you are not yet familiar with Equivalence Classes.

<a href="https://youtu.be/jf9hLsKE7U4?t=57"><img src="video-still.png" alt="overview video" width="400"/></a>


<tip>
    <p>
        It will help if you have read <a href="ec-r-value-settings.md">Setting Equivalence Classes and Representative</a> Values
    </p>
</tip>
<tip>
    <p>
        When you add a Method Component, an Instance Component will automatically insert an <a href="instance-component.md" >Instance Component</a> (the method's parent class) and a <a href="test-case-table.md">Test Case Table</a>. 
    </p>
</tip>

## 1. Add the Method
When you want to test a method, you use the Method component. To add a new one to the canvas

<img src="ec-method-search.png" alt="Class method search" width="600"/>

- Click on the + icon as shown in the image above to open the search dialog.
- Enter the name of the method you want to add (you can filter using the dropdown).
- Press the + icon to add to the canvas.

You should now see a new component on the canvas. The image below shows one, which has already been configured.

<img src="ec-method-empty.png" alt="method component"/>

<warning>
<p>
At the time of writing, you Custom Assertions and Side Effects are not implemented. These are coming very shortly.
</p>
</warning>

The Method component has several sections, divided into **Input** and **Output** columns.

## Input column
The Input column will contain several sections, one for each method parameter. You should create at least one Equivalence Class for each parameter with at least one Representative Value in each Equivalence Class.

## Output column
This is where you define possible/expected outputs from the method. These are divided into the following sections.

### Expected Values
Equivalence Classes and Representative Values for the expected values that are returned by the method.

### Exceptions
If your method throws Exceptions, you will want to specify the Exception type. For each different Exception type you expect, add a new row by hovering on the Exception section header and pressing the + icon. You select the Exception type from the dropdown. If you select **Exception**, then it will handle all Exceptions including custom exceptions.
### Custom Assertions
If you want to write your own code to handle the assertion. For a detailed explanation on how to define and code the Custom Assertion, [click here](custom-assertions.md).

### Side Effects
If your method a) doesn't return a value that you can test against and b) mutates the object properties such then you can use Side Effects to test against the state of the object after the method has executed. Please refer to the [Side Effects page](side-effects.md) for a more detailed explanation.

## 2. Add Equivalence Class(es)
You will typically have at least one Equivalence Class for each Input and Output. Vizitest creates Valid Values and Invalid Values for you by default.

Creating Equivalence Classes is described in detail [on this page](ec-r-value-settings.md#adding-an-equivalence-class-to-an-instance).

## 3. Add Representative Values
Each Equivalence Class will usually have at least one Representative Value.

Adding a Representative Value is described in detail [on this page](ec-r-value-settings.md#adding-a-representative-value).

The more Equivalence Classes and Representative Values you add, the more test cases you will end up with. So don't add unnecessary ones so the amount of Input/Output matching does not become unnecessarily large.

The method shown here is covered in a [training unit](simple-static-method.md).

## Training Unit
There is a [training unit](simple-static-method.md) that explains the Method Component based on a real code example. It also explain how Method Components are referenced when generating Test Cases.
