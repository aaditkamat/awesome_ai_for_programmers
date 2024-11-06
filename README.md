# Awesome AI for Programmers

In this repository, we collect all the most interesting things about using AI in software development.

## Cases with ChatGPT

ChatGPT and other LLM cases for developers

1. Writing code for a task, adding a feature to the existing code - for example, writing a function that sorts a list in ascending order.
1. Refactoring (splitting a long method into several short ones) - for example, splitting a long method that gets a list of users and returns the number of users with active accounts into several short methods.
2. Optimization
2. Writing tests for the code, generating tests for the interface - for example, writing test scripts for a function that returns the sum of elements in a list.
3. Prompt for naming tests in accordance with the rules set out in the book "Principles of Unit Testing" by Vladimir Khorikov below.
4. [Writing test code](https://github.com/di-sukharev/AI-TDD) (TDD) - for example, writing test scripts for a function that checks whether a number is prime.
5. Writing and optimizing SQL queries - for example, writing a SQL query that finds the number of users registered on a given day.
6. Converting SQL code to Entity Framework queries and vice versa - for example, converting a SQL query to an Entity Framework query that gets a list of users who have outstanding payments.
7. Code analysis: looking for stylistic errors, asynchrony/multithreading errors - for example, finding inefficient queries in code that fetches data from a database.
8. Code explanation - for example, explaining how an algorithm for finding the shortest path in a graph works.
9. Detailed error information - for example, displaying detailed information about an error that occurred during application execution.
10. Drawing diagrams and graphs (mermaid, [quickchart.io](http://quickchart.io/), Graphviz) - for example, creating a class diagram for an application.
11. Generating data - for example, generating an array of medical words that is used as input for an application.
12. Adding documentation to methods - for example, adding documentation to a method that returns the average value of elements in a list.
13. Generating documentation from code to markdown (dto to markdown) - for example, generating documentation from code comments in markdown format.
14. Converting code from different languages ​​- for example, converting Python code to C++ code.
15. Converting json to xml and vice versa - for example, converting a json file that contains user information to an xml file and vice versa.
16. Generate classes from json - for example, generate classes that represent entities in the application based on a json file that contains information about these entities.
17. Estimate the computational complexity of code
18. Escape data for code: for example, sometimes you need to throw json into a string variable or make a string from another code
19. Generate a class implementation based on an interface contract

## Prompts

### Prompt "Senior"

A universal prompt that improves the quality of refactoring/creating new code

```
Rewrite the provided in tripe backticks code like you are a Senior Software Engineer. Fix all code smells. Make the code perfect. Never use placeholders, shortcuts, or skip code. Always output full, concise, and complete code.
```

### Test Writing Expert

Prompt for creating and naming tests according to the rules described in the book by V. Khorikov "Principles of Unit Testing".

Please note that the prompt uses xUnit, FluentAssertions and Moq. You can replace these libraries with your favorites.

```
As a Senior Software Engineer and QA Expert, you will write tests in C# using the latest language syntax and the xUnit and FluentAssertions libraries for asserts.

Use the Arrange/Act/Assert approach.

It is important to cover 100% of possible cases.

Avoid placeholders, shortcuts, or skipped code, and always output full, concise, and complete code.

If you really need mocks, use the Moq library.

If you need clarification on the task, feel free to ask questions.

For tasks with more than 5 tests, please describe the test cases first and wait for user approval before implementing them.

When naming tests, follow provided in tripe quotes rules.

Naming rules:
"""
No rigid naming policy: Avoid using a strict naming convention, as it may not provide a high-level description of complex behavior. Allow freedom of expression.
Describe the scenario in plain English: Name the test as if you were describing the scenario to a non-programmer who is familiar with the problem domain, such as a domain expert or a business analyst.
Separate words by underscores: Use underscores to improve readability, especially for long test names.
Don't include the method under test in the test name: Focus on testing application behavior rather than specific code or methods.
Here are some examples to illustrate the transformation from a rigid naming convention
