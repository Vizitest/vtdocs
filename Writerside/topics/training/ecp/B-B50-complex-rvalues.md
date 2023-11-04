# Complex Representative Values
**Repo folders** 
- [src/main/java/B_B50_Money/Money](github-repo.md)
- [src/main/java/B_B50_Money/Transaction](github-repo.md)

## Prep
- Find and open the training code.
- Examine the code to see what it's doing.
- In the Test Manager, [create a new Test Configuration](test-config-add.md) called **Complex Args**. 
- Open the new Test Configuration.

## Introduction
Complex data types will be used extensively in your code and so you need to understand how to work with these in Vizitest.

## Task

### A basic complex argument
We will assume you know how to add the Instance component from the [earlier lesson](B-B40-water-state-instance-1.md).

1. Search for and add an Instance component for ```B_B50_Money.Money```
2. You should see an empty Instance Component on the canvas.
3. Add a Representative Value in the **Valid** Equivalence Class.
4. Click on the newly added value. Uou'll see the complex type ```Money``` ready for editing.

<img src="training-complex-simple.png" alt="complex r value simple" width="500"/>

That's all there is to a basic complex argument. Now let's look at a nested complex argument.

### A nested complex argument

1. Search for and add an Instance component for ```B_B50_Money.Transaction```
2. You'll see an empty Instance Component on the canvas.
3. Add a Representative Value in the **Valid** Equivalence Class.
4. The component should now look like this. You can see that it is a complex object with two properties, ```transactionId``` and ```money```.

<img src="training-complex-nested-1.png" alt="complex r value nested part 1" width="600"/>

5. Now click on the value and you'll see it expand. We can edit ```transactionId``` directly. However, money is also a complex type, 

<img src="training-complex-nested-2.png" alt="complex r value nested part 2" width="600"/>

6. Click on the ```money``` value. It will now expand into a nested value. This you can edit directly as it contains no complex types.

<img src="training-complex-nested-3.png" alt="complex r value nested part 3" width="600"/>

7. Add some data into the deepest ```money``` object and press the green check mark to save it. Do the same for the topmost object and save that, too. You should now see something like this.

<img src="training-complex-nested-4.png" alt="complex r value nested part 4" width="600"/>

You can see how 




