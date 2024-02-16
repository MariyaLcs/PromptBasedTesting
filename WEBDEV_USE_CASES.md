# Use Cases, Prompts, and Examples

This document outlines various use cases, prompts, and examples from my experience with applying ChatGPT in web development and testing scenarios. Each section provides a detailed look at how specific prompts can be used to solve problems, automate tasks, or enhance the development process.

## Table of Contents

- [Use Case #1: Testing for Edge Cases](#use-case-1-testing-for-edge-cases)
- [Use Case #2: Generating Edge Cases with Console.log Examples](#use-case-2-generating-edge-cases-with-consolelog-examples)
- [Use Case #3: Writing Jest Tests](#use-case-3-writing-jest-tests)

## Use Case #1: Testing for Edge Cases

### Context

Identifying edge cases for a JavaScript function that calculates a person's age, aiming to ensure comprehensive test coverage.

### Prompt

"I have a JS function to calculate the age of a person based on input. List 8 edge cases this function should account for, and provide test cases for each, described in a single sentence."

### ChatGPT Response

- Future Birth Date: If the birth date is after the current date, return an error.
- Leap Year Birth Date: Ensure accurate age calculation for leap years.
- [Additional cases as described]

### Outcome and Reflections

This prompted a more thorough approach to test planning, highlighting the importance of covering a wide range of input scenarios.

## Use Case #2: Generating Edge Cases with Console.log Examples

### Context

Expanding on identifying edge cases by providing `console.log` examples for direct implementation in code.

### Prompt

"Give me the edge case tests in a single code block, and denote the edge case as part of the console.log."

### ChatGPT Response

```javascript
// Example edge case tests
console.log("Future Birth Date", calculateAge("2025-02-12")); // Expected: Error
console.log("Leap Year Birth Date", calculateAge("2000-02-29")); // Expected: Correct age
// Additional examples as provided
```

### Outcome and Reflections

The detailed response was exceedingly useful for visualizing and implementing tests directly in the code, making it a practical example of how to apply ChatGPT's suggestions. This method not only aids in test development but also serves as an educational tool for understanding and anticipating potential issues in software functions. For future enhancements, incorporating these tests into a continuous integration pipeline could automate the validation process, ensuring that the function behaves as expected across all identified edge cases.

## Use Case #3: Writing Jest Tests

### Context

The focus here was to create a series of Jest tests for a simple `isEven` function, which checks whether a number is even. The intent was to ensure the function's robustness across a variety of inputs, including different number types and values that could be considered edge cases, thereby enhancing the function's reliability in practical applications.

### Prompt

"Write 10 tests for the `isEven` function using Jest."

### ChatGPT Response

```javascript
describe("isEven", () => {
  test("should return true for 2", () => {
    expect(isEven(2)).toBe(true);
  });

  test("should return false for 3", () => {
    expect(isEven(3)).toBe(false);
  });
  test("should return true for 0", () => {
    expect(isEven(0)).toBe(true);
  });

  // The response continued with additional tests...
});
```

### Outcome and Reflections

The response provided a solid foundation for testing the isEven function, covering basic cases of even and odd numbers, including edge cases such as 0. This exercise was particularly useful as it not only supplied potential test cases but also hinted at the next steps for refining the function itself. For instance, it exposed considerations for how the function might treat string inputs that can be coerced into numbers, suggesting areas for improvement in type checking and validation within the function.

This case underscores the value of using automated testing to not only verify expected outcomes but also to enhance the robustness and reliability of functions by identifying and addressing edge cases and potential ambiguities in input handling.
