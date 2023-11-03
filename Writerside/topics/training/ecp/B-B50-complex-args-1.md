# Complex Arguments
**Unit B-B50** / **Repo folder : B_B50_PersonSimple** 

## Prep
- Find and open the training code **B_B50_PersonSimple** you [cloned from GitHub](github-repo.md).
- Examine the code to see what it's doing.
- In the Test Manager, [create a new Test Configuration](test-config-add.md) called **Complex Args**. 
- Open the new Test Configuration.

## Introduction
Complex data types will be used extensively in your code and so you need to understand how to work with these in Vizitest.

They are relevant in Representative Values, whether in an Instance or Method component.

## Task

### Add an Instance component
We will assume you know how to add the Instance component from the [earlier lesson](B-B40-water-state-instance-1.md).

1. For this example, we need one Representative Value in the **Valid** Equivalence Class. Add the **Valid** Equivalence Class and add the Representative values ```John Brook``` and ```35```.
2. This value is a complex arg. It's really not difficult.

[TODO : check the constructor process and how it's described above and documented below]

[TODO : what happens with the output when dob is null, which it is using the simpler constructor]

### Add a Method component
Use the **+** icon to search for and add the ```getSummary()``` method. 

As ```getSummary()``` expects no parameters, we don't need to worry about the Input section.

Only the following needs to be configured
   1. Input - nothing required as there are no parameters
   2. Output -> Return Values - here we need to check the expected value returned from the method, which should be ```John Brook is 35 years old```, so add this as the value.

### Configure the Expected Values 
We need to handle the Expected Value. 

As you can see from the code, it simply concatenates the name and age. So, make sure that there is a valid Equivalence Class with the Representative Value set to ```John Brook is 35 years old```

That's it. Your configuration should now look like this. 

<img src="r-value-complex-1.png" alt="complex r value" width="400"/>

[TODO : correct screenshot above]

### Generate and run test
1. Generate the test cases.
2. Set the Outputs.
3. Generate the test code .
4. Run the test in your IDE.

### Things to try
- Try changing the Representative Values so the test fails.
- Change the code so the test fails with a properly configured Test Configuration.


