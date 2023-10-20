# Side Effects
**Unit C-I70** / **Repo folder : C_I70_SideEffects** 

[TODO - WHOLE REVIEW ONCE AVAILABLE]

## Prep
- Find and open the training code C_I70_SideEffects you [cloned from GitHub](github-repo.md).
- In the Test Manager, add a new Test Configuration **Side Effects**. 
- Open the new Test Configuration.

## Introduction
You will use Side Effects when you want to determine test case outcomes based on object mutation by a Method Under test rather than using Expected Values.

Let's look at the code in our code example.

```
public class SideEffects {
    private double currentValue;

    SideEffects() {
        this.currentValue = 100;
    }

    public void multiplyBy(double multiplicand) {
        this.currentValue *= multiplicand;
    }
}
```

Assuming we want to test the method ```multiplyBy(double multiplicand)``` we can see

- it's a ```void``` function, so we **can't** use the Expected Value approach
- and it mutates the object.

This means the only way we can test is to examine the state of the Instance after the method has executed.

Please refer to [Side Effects](side-effects.md) for detail on how to configure a Side Effect.

## Task

### Instance
- Create an Instance of the ```SideEffects``` class.
- There is no need to add any Equivalence Classes as the ```currentValue``` property is initialized with a value of ```100``` by the constructor.

### Method
1. Add a Method component to test the ```multiplyBy()``` method.
2. Create a single valid Equivalence Class with the Representative Value ```5```.
3. Add a valid Equivalence Class with a Representative Value of ```500``` in the Verification -> Side Effect section.
4. Generate the test cases in the Test Case Table and set the Verification within the Side Effects row.
5. Press **Generate code** and then run the generated test. It should pass.

