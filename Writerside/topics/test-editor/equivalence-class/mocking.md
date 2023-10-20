---
sidebar_position: 110
---

# Mocking and Stubbing
This page assumes familiarity with the concept of mocking and stubbing. 

One of the next things we will be building is explicit UI support for mocking within Vizitest. We anticipate this being ready in October 2023.

In the meantime, it is still possible to mock, but it requires you to use a [User Method](ec-r-value-settings.md#instantiating-with-a-user-method).

You can define a User Method to support your mocking when setting any Representative Value. Once defined, it can be re-used, so you only will need to define it once.

## Example
Consider the following class ```UserService``` and assume we want to create a unit test for ```simpleAddUser()```.

![](mock-service-source.png)

You can see that ```simpleAddUser()``` is dependent on the external method ```addUserRepository.execute()```.

In order to create a unit test, we will need to use a test double in order test ```simpleAddUser()``` in isolation.

### Creating the User Method
Go to the Representative Value you want to work with a select it. From here you can [create your new User Method](ec-r-value-settings.md#instantiating-with-a-user-method).

![](mock-mock-config.png)
[TODO : replace once User Method fixed with type dropdown/search]

You can see how we are creating a User Method called ```mockSimpleAddUserRepository``` with the three parameters ```name```, ```age``` and ```bio``` that are required to instantiate the ```User``` object.

### Setting the Representative Value 
Having done this, we can set the Representative Value to whatever we want by selecting the mockSimpleAddUserRepository User Method and setting values as you like.

[TODO : screenshot once we have an example done]

### Coding the User Method
Once you have generated your test cases from the [Test Case Table](test-case-table.md), you can generate the test code.

Open the [generated test code](codegen.md) and look for your User Method.

![](mock-test-code-pre.png)

You can then modify the auto-generated boilerplate.

![](mock-test-code-post.png)

### Mocking Framework
You are free to use your preferred mocking framework using this approach as the implementation of the User Method is fully under your control.

