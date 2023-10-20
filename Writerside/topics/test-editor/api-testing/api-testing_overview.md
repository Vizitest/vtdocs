# Overview
** *Available in Q1 2024 with REST support.* **

There are plenty of ways APIs can be tested using 3rd party tools such as Postman or manually coded test frameworks.

So, what can I do with Vizitest and what is different to other products on the market?

## Endpoint **and** code level testing
A key capability of Vizitest API is the ability to test in two completely different modes.

- **Endpoints** - test in development, staging or production by passing a payload to an actual http endpoint. Can be executed manually or under a test runner.
- **Code** - create a code level integration test that runs under your test runner and fits into your development pipeline.

The combination of these gives you the most rigorous testing setup and the most timely detection of issues.

## User friendliness
One of our main goals is to provide an environment where tests are 

- nicely organized using the Test Manager and 
- visually configured using the Test Editor.

[TODO : screenshot of Test Manager + Method for now until new component is added]

## API schema
There are two ways to discover the schema of any API call.

- Automated - point it to an OpenAPI specification.
- Manual - define the schema by hand.

Once this is done, you're ready to start defining your input data.

## Input and expected output data
Because Vizitest API plugs into the regular Vizitest UI, you can define valid and invalid Equivalence Classes along with their Representative Values. 

This is not just a nice way of defining your input and expected output data structures but also the basis for a key part of true quality-oriented testing - the automated generation of Test Cases.

[TODO : screenshot]

## Security, Authentication and Headers
Vizitest lets you configure sensitive variables such as secret keys and other data that you might store in a ```.env``` or similar file. This data is only stored locally and will not be committed to the codebase repository.

Vizitest API will also support Basic Authentication and OAuth.

REST Headers can also be configured.


## Automatic Test Case Generation
Generating the right number of Test Cases is a critical part of testing when you are not only interested in code coverage but also ensuring that the requirements are met - one of the best ways of delivering quality.

Calculating the right number of Test Cases is non-trivial. Doing it manually will usually result in you either not crating enough Test Cases (quality suffers) or writing unnecessary Test Cases (time wasted).

Vizitest uses a dedicated algorithm to generate the optimal number of Test Cases for you.

## Test Execution
Vizitest offers two modes of running your tests. 

- **Manual** - run a test directly from Vizitest and then provides the test results on screen.
- **Test Runner** - tests run under your regular test-runner such as JUnit with results reported therein.

In both cases, all of the auto-generated Test Cases are executed for your and you will see clear reports showing the status of the test with details of which Test Case has passed or failed.

## Plays nicely with Git
Your Test Configurations are store within a codebase or a file location that can be committed to a Git repository.

The advantage of this is that it keeps everything away transparent and from the Cloud but still allows everything to be shared.

