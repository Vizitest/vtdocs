# The AI problem

>*"I thought letting ChatGPT write my tests was a great idea. I'm now running into serious maintenance problems and each test looks completely different."*

## Research summary
David Farago in his paper "Engineering a Reliable Prompt for Generating Unit Tests"  summarised the problems with AI generated tests by concluding that _"... in general, AI can achieve software engineering tasks like test case generation, but full robustness, correctness, and comprehensiveness are hard to achieve..."_

## The Problem
If you really care about quality, then you should not leave your unit and integration tests to chance. That is what you'll be doing if you use AI to generate your tests.

A engineers, we hope that AI will be silver bullet. It turns out that it is more often than not a lead balloon.

Of course AI has a lot to offer in the field of code generation, but we think AI should be used where it delivers net positive value, see [The Future of AI in Vizitest](#the-future-of-ai-in-vizitest).

Getting good code coverage is fairly easy use AI generated tests. Of course, even with excellent coverage ([see The Code Coverage problem](code-coverage.md)) there are a lot of questions you will need to (or certainly should) answer.

- What technique did the AI use the generate Test Cases.
- Has it generated the right number of test cases to deliver quality.
- What parameters and data did it choose for the tests? Were they really appropriate values?
- How readable is the code it generated? AI will take code from all sorts of sources, so there will be no consistency of style, which matters if you have to debug hundreds or thousands of tests.

Answering these questions so that you are convinced of the quality of AI tests, will take a considerable amount of time for all but the simplest tests. Not bothering to answer these questions will either result in false positives or false negatives that will sooner or later take a lot of time to diagnose.

### Test maintenance hell
Using AI looks at your functional implementation and then generates a White Box test.

This means that if your requirements change and the test fails, you will be forced to decipher the AI generated code, which will not be in a consistent style and likely be very tricky indeed to figure out.

Initially, this will seem like an innocuous problem and one that you might choose to oversee as you get great code coverage results - even though it might not actually meet the requirements. 

Over time, though, these problems will add up, and you'll spend so much time debugging the test that you'll likely end up simply disabling many tests for expediency reasons. And so you lose all the benefits of testing.

## Integration tests
AI is not well suited to more complex testing scenarios in most cases. It cannot be expected to understand the combination of method calls you want to use.

## The Solution
Vizitest's guiding principle is to allow you to decide which Test Type you want to use, then apply some thought to the requirements mapping before  auto-generating your test cases and test code.

However, configuration with Vizitest is quick and almost everything else is automated.

Furthermore, Vizitest solves the readability problem and generates highly consistent, self-documenting code that will run independently of Vizitest. Even for complex testing scenarios.

So, if you decide to stop using Vizitest for any reason, your tests will still run.

## The future of AI in Vizitest
Having considered using AI when we started out, we soon decided against it, even though implementing it would have been straightforward. We'd get great code coverage but great quality would not be assured, and our users would be storing up test maintenance hell.

We will be using AI as follows

- We will provide a UI for specifying requirements in a structured fashion.
- We will build our own model for this, which will avoid sending any of your code into the cloud.
- AI will then translate these requirements into Equivalence Classes and Representative Values.
- Form this point on, our Test Type algorithms will handle the auto-generation of Test Cases and Test Code in a way that AI cannot rival.

Even here, to ensure quality, we will advise users to carefully inspect the Equivalence Classes and Representative Values to validate the job that AI has done.
