# Instance component
Please note that you will need to instantiate a Class component whenever you want to test a non-static method belonging to that Class.

<tip>
    <p>
        Instance Components are automatically added when you add a Method Component, so you don't have to manually insert one.
    </p>
</tip>



[TODO - if we add a method but there is no Instance component related to that Class, can we add the Instance component automatically?]

## 1. Find the Class
You first need to find the Class you want to instantiate.

<img src="method-class-search.png" alt="method class search" width="400"/>


- Click on the + icon to open the search
- Start typing the name of the Class
- You can select Class from the dropdown to filter only Classes if you want
- Click the + icon next to the instance

You should now see your Class added to the canvas as a new Instance component.

## 2. Add Equivalence Classes
Vizitest creates two commonly named, default Equivalence Classes **Valid Values** and **Invalid Values**.

If you want to add new Equivalence Classes then [click here](ec-r-value-settings.md#adding-an-equivalence-class-to-an-instance) for instructions.

## 3. Add Representative Values
Each Equivalence Class should have at least one Representative Value.

Adding a Representative Value is described in detail [on this page](ec-r-value-settings.md#adding-a-representative-value).

If there is only a default constructor or one without arguments, then you should still add a Representative Value.  [TODO - Daniel please provide explanation on this]

The more Equivalence Classes and Representative Values you add, the more test cases you will end up with. So don't add unnecessary ones so the amount of Input/Verification matching does not become unnecessarily large. [TODO - Daniel, not completely happy with this statement and it may be wrong!!!]

[TODO - explain how the ECs are related to the TCT once the TCT is working]




