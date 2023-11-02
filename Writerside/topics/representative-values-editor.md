# Representative Values Editor
**Repo folder** : [src/main/java/playground/*](github-repo.md)

The Representative Value editor lets you create values for many different types.

## Simple values
Open the class ```src/main/java/playground/TypeTester``` in your IDE.

You will find some simple methods that are designed to show the Representative Value editor in action for different simple values.

- In the Test Manager, create a Test Configuration for each of the methods.
- Within the Test Configuration, add the appropriate [Method Component](method-component.md).
- In the Input column, add a single Representative Value within the **Valid Values** Equivalence Class.
- You can then play around and edit the value.

### Primitive values
These should be self-explanatory. You have already dealt with primitive types in earlier training units but there are some

### Arrays, Lists and Enums
These are a little more involved. Add a Representative Value and add some values.
[TODO once ready; screenshot]

## Complex Values
### Basic

- Locate the ```Money``` class in ```src/main/java/playground```.
- In the Test Manager, create a Test Configuration called **Complex - Money** and open it.
- Add Money.getMoney from the + button (be sure to add the one indicated as there are two methods with the same name).

<img src="training-rvalues-search.png" alt="search" width="600"/>

- You will now see and Instance and a Method Component added to the canvas.
- You can see below that there's a value already added and selected in the Instance Component.
- The Return Value expects the same object that was passed in and so you see the same value editor layout.

The ```Money``` data type has no complex values as arguments. The next example will, however.

<img src="training-rvalues-money.png" alt="instance and money components" width="900"/>

### Nested
In this example, we'll show a complex data type that has another complex data type as an argument.

- Locate the ```Transaction``` class in ```src/main/java/playground```.
- In the Test Manager, create a Test Configuration called **Complex - Transaction** and open it.
- Add Transaction.getMoney from the + button (be sure to add the one indicated as there are two methods with the same name).

<img src="training-transaction-search.png" alt="instance and money components" width="600"/>

- You will now see and Instance and a Method Component added to the canvas.
- You can see below there's a value already added and selected to the Instance Component.
- Note how one complex value is nested within another.
- The Return Value is also complex but is not nested as Money does not have complex arguments.

<img src="training-transaction-nested.png" alt="instance and money components" width="900"/>



