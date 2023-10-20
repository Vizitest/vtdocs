# Theory

The goal of this page is to define and explain three important terms

- Equivalence Class
- Representative Value
- Boundary Values

## Requirements
Let's start off with a simple requirements statement as a backdrop. Physicists might want to argue about the temperatures used, but we're keeping it simple!

**We have a method that expects a temperature of water to be input. It should return the state of the water as a string.**

- The input parameter should be a floating point value
- The method is expected to return ```solid``` if the temperature is ```<=0```
- The method is expected to return ```liquid``` if the temperature is ```>0``` and ```<100```
- The method is expected to return ```gas``` if the temperature is ```>=100```
- It should throw an exception if the temperature is below absolute zero, ```<273.15```

## What is an Equivalence Class?

***An Equivalence Class is a named set of values, each of which is considered to be representative of that set and the behavior of the system is the same or Equivalent.***

To illustrate this, lets look at the state of water at different temperatures. There will be those who want to argue about exactly when water freezes or turns to steam, but for the sake of simplicity, let's assume it is at 0 and 100.


<img src="ec-definition.png" alt="example" width="500px"/>

Let's assume we have a method that returns the state based on temperature as an input value.

```
string getWaterState(double temperature) {
  ....
}
```

From the requirements and the above example, we can say

- We have four Equivalence Classes - **Solid**, **Liquid**, **Gas** and **Invalid**. 
- Within each Equivalence Class, every temperature value is equivalent with respect to the output returned by ```getWaterState()```.


## What is a Representative Value
A Representative Value is a single value that you choose that "represents" the class to which it belongs. So in our example we could choose

- **Ice** : any negative value  up to ```-273.15```, for example ```-10```
- **Water** :  any value between ```0``` and ```100``` for example ```50``` 
- **Steam** : any value over 100, for example ```1000```
- **Invalid** : any negative value below ```-273.15```, for example ```-300``` or a value that is not compatible with the ```double``` data type sch as ```"some string"```

Assuming you have correctly defined your Equivalence Classes, it really doesn't matter which value you choose for each one.

## Boundary Value Analysis
It is shown that a large number of software errors occur at "boundaries". Our example actually illustrates this nicely. When exactly does water freeze? Is it ```=0``` or ```<0``` or ```>0```? We've defined this in the requirements, but you can see how easy it is to introduce an error by making a mistake with  ```=```,  ```<```, ```>+``` etc.

The way you decide on this is reflected in the way you have coded your method. They way that it has been coded should reflect the requirements specified. It is how the Engineer has implemented the requirements that matters. 

So for our examples, you would want to very specifically test the following boundary values.

- ```-273.15```, ```0```, ```100```

But you also want to test either side of the boundaries, so the full set to test might now be

- ```-273.16```, ```-273.15```, ```-273.14```, ```-0.5```, ```0```, ```+0.5```, ```99.5```, ```100```, ```100.5```

## From Theory to Practice
Now that we've defined the terms we'll be working with, let's put it all into practice with Vizitest in the [next section](practice-ecs.md).

