# Instance component
Please note that you will need to instantiate a Class component whenever you want to test a non-static method belonging to that Class.

<tip>
    <p>
        Instance Components are automatically added when you add a Method Component, so you don't have to manually insert one.
    </p>
</tip>

<tip>
    <p>
        It will help if you have read <a href="ec-r-value-settings.md">Setting Equivalence Classes and Representative</a> Values
    </p>
</tip>

## 1. Find the Class
You first need to find the Class you want to instantiate.

<img src="method-class-search.png" alt="method class search" width="500"/>

- Click on the large, blue + icon to open the search
- Start typing the name of the Class
- You can select **Class** from the dropdown to filter only Classes if you want
- Click the **+** icon to the right of the instance to insert into the canvas.

You should now see your Class added to the canvas as a new Instance component.

<img src="method-empty-instance.png" alt="empty instance component" width="600"/>


## 2. Add Equivalence Classes
Vizitest creates two commonly named, default Equivalence Classes **Valid Values** and **Invalid Values**.

If you want to add new Equivalence Classes then [click here](ec-r-value-settings.md#adding-an-equivalence-class-to-an-instance) for instructions.

You can also rename them by clicking and editing.

## 3. Add Representative Values
Each Equivalence Class usually has one or more Representative Values.

<img src="ec-instance-completed.png" alt="configured instance component" width="600"/>

Adding a Representative Value is described in detail [on this page](ec-r-value-settings.md#adding-a-representative-value).

The more Equivalence Classes and Representative Values you add, the more test cases you will end up with. So don't add unnecessary ones so the amount of Input/Output matching does not become unnecessarily large.

## Training Unit
There is a [training unit](B-B40-water-state-instance-1.md) that explains how to add an Instances using real code.

This explains how to configure an Instance and, in [Part 2 of that unit](B-B40-water-state-instance-2.md), how Instance Components are referenced when generating Test Cases.



