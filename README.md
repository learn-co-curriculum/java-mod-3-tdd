# Test Driven Development

## Learning Goals

- Introduce Test-Driven Development (TDD).
- Explain the benefits of TDD.

## Introduction to Test Driven Development

Test Driven Development (TDD) is the practice of writing unit tests _prior_ to
implementing the functionality that is meant to be tested. This may sound
counter-intuitive, but it has the following benefits:

- Unit testing forces us to think about the structure of the code and making
  sure the code is written in a way that it can actually be tested. Going
  through that process prior to actually writing the code saves time and leads
  to better written software sooner.
- It forces us to have the mindset of "if we cannot test it, we cannot write the
  code." We cannot write code that isn't covered by unit tests.

The common steps to TDD are the following:

1. Write a unit test to test a certain functionality.
2. Run the test (which will fail the first time around since we have not written
   any code yet in the program).
3. Write some code and/or refactor the code to make the test pass.
4. Execute the test(s) again and see if it passes.
   1. If it does not, go back and refactor the code until it does pass.
5. Repeat the following steps by adding unit tests any time we want to add
   additional features or functionality.

Below is a diagram illustrating the lifecycle of test driven development:

![tdd-cycle](https://curriculum-content.s3.amazonaws.com/java-mod-3/tdd/tdd-cycle.png)

Note that we "stop" or end the cycle when we are finished developing the
program.
