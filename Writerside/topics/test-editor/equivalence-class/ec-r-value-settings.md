# Setting Equivalence Classes and Representative Values
Please refer to the Equivalence Class [Theory](theory-ecs.md) and [Practice](practice-ecs.md) pages if you are not yet familiar with Equivalence Classes.

You will use Equivalence Classes extensively in the Instance and Method components. This describes how to set them

## Instance Component
This shows an Instance Component with one Equivalence Class. It contains three Representative Values with a complex type being passed via a constructor.

<img src="instance-component-example.png" alt="" width="500"/>

## Method Component
This shows a Method Component with valid Equivalence Classes. You will see promitive Representative Values in ```int creditSought``` and complex in **Return Values**.

<img src="method-component.png" alt="" width="900"/>

## Adding an Equivalence Class to an Instance

<img src="instance-annotated.png" alt="" width="700"/>

1. Press the large + icon in the top right of the component to add a new Equivalence Class.
2. Toggle between a valid and invalid type by clicking the icon. The icon will toggle between green and red.
3. Change the name of the Equivalence Class to something meaingful. Well-chosen names will help when running your tests (and looking at the generated code) as they will appear as labels and comments.

## Adding an Equivalence Class to a Method

<img src="method-annotated.png" alt="" width="500"/>


1. Press the + icon in one of the section header bars. This will appear when you hover over it.
2. Toggle between a valid and invalid type by clicking the icon. The icon will toggle between green and red.
3. Change the name of the Equivalence Class to something meaningful. Well-chosen names will help when running your tests (and looking at the generated code) as they will appear as labels and comments.
  
## Adding a Representative Value
Hover over an Equivalence Class name and press the **+Add** button.

### Changing a primitive value
This is straightforward. Click on any value as highlighted below.

<img src="r-value-primitive.png" alt="" width="300"/>

You can then enter the value directly in the field.

### Changing a complex data type
Complex data types are summarized as json in the value field as shown below. You can see that there are three values already entered.

This is an Instance component and the Class constructor has two parameters. ```String name``` can be edited in place.

However, ```LocalDateTime dateOfBirth``` is a complex data type.

<img src="r-value-complex-0.png" alt="" width="600"/>


To edit, click in the value field and it will expand. 

<img src="r-value-complex-1.png" alt="" width="600"/>

You can see here that we are able to choose the constructor to use when instantiating the object. You can change the constructor here by clicking an orange constructor pill.

The ```String name``` field can be edited in place but ```LocalDateTime dateOfBirth``` cannot, so we click on this field to edit it.

A new, nested area will appear where you can edit each of the values.

<img src="r-value-complex-2.png" alt="" width="600"/>

### Arrays, lists and enums
The Representative Value editor has the following behavior when working with these data types. The following screenshot highlights an array and a list.

<img src="ecp-array-rvalue.png" alt="arrays lists and enums" width="800"/>

When you click in an array, list or enum field, you can add new array items by pressing the + icon (circled). To save and collapse the items, press the icon to the right of + icon.

There is a training unit that covers these data types.

- [Arrays, lists, enums](arrays-lists-enums.md)

### Generics

<warning>
<p>
Generic types are coming very soon.
</p>
</warning>

### Collapsing, saving, discarding
Any complex data type values you have edited will leave the expanded section open until you explicitly change it.

You can discard changes by pressing the X button or keep them by pressing the ✓ button.

## Instantiating with a User Method
With complex data types, Vizitest will use a constructor to instantiate a Representative Value by default. If there a multiple constructors then you can choose which constructor to use.

However, you can also instantiate it with your own (factory) method. Select the Representative Value and press the **+ User Method** button.

Any previously defined User Methods are shown in a light blue color and can also be selected.

<img src="user-method-1.png" alt="" width="400"/>

You will then see the following dialog.

<img src="user-method-2.png" alt="" width="400"/>

You will notice that the return tpe is automatically set to the data type of the instance's class.

- Enter the name of the new method. Use the normal method naming conventions, so no spaces etc.
- Press the **+** button to add as many parameters as your method requires.
- specify the data type (**Full type name**) and parameter name (**Name**) for each added parameter.
- Press **Add** to save and close the dialog.

You will now see your new method added, as a blue pill, and selected. The parameters you defined (```int age``` and ```double amount```) can now be edited.

<img src="user-method-3.png" alt="" width="400"/>

### User Methods without parameters
There are rare cases when you might want to use a User Method without any parameters. A typical example would be if you are using the **Object Mother Pattern**.

### Implementing your User Method
The User Method generates method boilerplate for you when the test code is generated. You can then write the necessary code in that method to handle the instantiation.

If you open the generated test (**Generate Code** button in the [Test Case Table](test-case-table.md)) then you will see the boilerplate ready to edit.

```java
//region Factories
	private static CreditCheck MyFactoryMethod(Integer age, Double amount) {
		// TODO implement factory
		throw new UnsupportedOperationException();
	}
//endregion
```

You can now replace the lines

```
  // TODO implement factory
  throw new UnsupportedOperationException();
```

...with your own implementation. Note that the return type, ```CreditCheck``` in the above example, is automatically provided in the method signature.


