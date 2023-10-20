# Equality Check
As a matter of good practice, you should implement the equality check for data type objects where object comparison is necessary.

- In Java this is the ```equals()``` method.
- In C# it's the ```Equals()``` method.

With testing in general, many tests will want to assert whether ObjectA == ObjectB. 

Your test framework would then use the ```equals``` assertion. If the equality check does not exist, you will get an error like this (depending on IDE and language).

![](ug-implement-equals.png
)
