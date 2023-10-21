#Adding More Equivalence Classes and Representative Values
**Unit C-I60** / **Repo folder : C_I40_MultipleMethods** 

You may have asked yourself what are the consequences of adding 

- more and more Representative values within a single Equivalence Class
- more Equivalence Classes.

In theory, you should only add the right number of each. Not too many, and not too few. 

You configure your test based on the requirements and there will be a minimum number of Equivalence Classes you would add to configure an adequate test that meets the requirements. 

Within each Equivalence Class, you would choose the minimum number of Representative Values to perform the test adequately.

You should be aware, though, that the more Equivalence Classes and Representative Values you add, the more Test Cases will be generated, if you choose to ask Vizitest to auto-generate test cases. 

While there is nothing inherently wrong with this, you should be aware of the following.

- Your test will take longer to run the more test cases you have. This doesn't matter for a smaller number of test cases but could impact speed when there is a large number of test cases.
- You need to match the Expected responses to the auto-generated inputs in the Test Case Table. If you have a large number, this will take longer.

## Prep
- Find and open the training code C_I40_MultipleMethods you [cloned from GitHub](github-repo.md).
- In the Test Manager, clone the  **Multiple Methods** Test Configuration we created in the [previous unit](C-I40-multiple-methods.md) and call it **Lots of Test Cases**. 
- Open the new Test Configuration.

## Task
When making the following changes, take a look at the number of Test Cases before regenerating the table. This way you can see what impact the changes have.

In the Test Editor, modify the Test Configuration. The following are suggestions, you can modify as you like.

- Add a valid Equivalence Class to either of the method Inputs and add another valid value. Then regenerate the Test Case Table and see what changes.
- Add a new Representative Value to an Equivalence Class. Then regenerate the Test Case Table and see what changes.
- Add a couple of your own experimental changes.
- Generate the test code and run the test to see how the test output changes.
