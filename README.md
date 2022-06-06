# Test Driven Development

## Learning Goals

- Explain TDD and how it's useful for development

## Test Driven Development

Test Driven Development is the practice of writing unit tests _prior_ to
implementing the functionality that is meant to be tested. This may sound
counter-intuitive, but it has the following benefits:

- Negative testing: it's possible that you write a unit test for a component,
  and it passes because it doesn't test the functionality you're targeting,
  versus passing because it tests the targeted functionality and that
  functionality is implemented properly.
- Unit testing forces you to think about the structure of your code and making
  sure your code is written in a way that it can actually be tested. Going
  through that process prior to actually writing the code saves time and leads
  to better written software sooner.
- If you cannot write functionality for which you have no unit tests, you cannot
  write code that isn't covered by unit tests.

Let's consider our "FizzBuzz" example from the previous section, with one more
level of complexity: we need to apply this FizzBuzz logic to an array by
replacing each individual value in the array with its FizzBuzz-based
replacement.

Thinking through this problem with TDD, we would take the following steps:

1. Create a `fizzBuzz()` method that does returns `null`
2. Write a test to validate the "start with f" scenario
3. Test fails
4. Add logic to `fizzBuzz()` to support that scenario

Rinse and repeat for all scenarios, including passing a `null` string.

Then, and only then, think about applying `fizzBuzz()` to each element in an
array:

1. You already have a `fizzBuzz()` method that you know works for a single
   element, so you will naturally leverage it when processing multiple elements
2. Create a method `fizzBuzzArray()` that takes an array as a parameter and
   returns `null`
3. Write a test that validates that a sample array is transformed properly
4. Test fails
5. Implement the functionality to process the array with the help of
   `fizzBuzz()` method

There is a very important observation to make here. Your test that validates the
processing of the array does not need to go through every single combination of
the `fizzBuzz()` scenarios, because it's re-using the `fizzBuzz()` method, so as
long as that method works properly _and_ the `fizzBuzzArray()` method properly
breaks down the array and passes its values properly to the `fizzBuzz()` method,
all the "FizzBuzz scenarios" will be covered successfully.
