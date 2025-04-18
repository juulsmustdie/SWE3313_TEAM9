# Team 9's Coding Style Guide 

This document goes over the coding conventions and practices all developers on the team _must_ follow to create consistent, readable, and maintainable code for our application.

The goal is to plan coding beforehand in order to achieve code that has minimal defects/bugs, improve productivity, and go over any possible issues that may occur and know how to solve them.

_Remember, all contributions should feel like they were written by the same person, not just a jumble of random pieces smushed together._

---

## Official Python Style Guide

We will follow [**PEP 8 – the official Python style guide**](https://peps.python.org/pep-0008/) and refer to the [**Introduction to Flask guide**](https://www.geeksforgeeks.org/flask-tutorial/) for tutorials/help regarding Flask.

### Important things to consider while coding include: 

- Spaces between code and proper indentations improve readability.
  
- With the previous point in mind, avoid cramming too much on a single line to maintain readability and traceability in your code (refer to IDE's visual guide for character limit).
  
- Use meaningful, descriptive names for variables, functions, and files to avoid any confusion and ambiguity.
  
- Be sure to keep names as short/clean as possible, excessively long names aren't great either.
  
- _**Prefer clarity over cleverness**_ — code should be self-explanatory and easy for the next person to read/pick up for future versions.
  
- EVERYONE is responsible for checking all code, even if they did not write it. If one part of the application fails, the entire thing fails.
  
- Comments are your best friend. Leave helpful comments to explain what's going on or why you implemented something.
  
- Feedback is extremely important when it comes to coding in a team. If you see parts that need improvement, say something and work together to fix it.
  
- _Do not wait until the last minute to test parts of the application_. Consider any and all possible risks and test your software as needed.

---

## Automated Test

 - Use _pytest_ for writing and running automated tests.

- Place all test files inside a tests/ directory to keep it organized.

- Test files should be named with "test_" prefix, such as test_*.py, to avoid mixups and confusion.

- Focus on:

    - Unit testing core logic and endpoints.

    - Validating input/output.

    - Edge cases.

---

## Integration Testing

- **Integration tests should be done periodically** —
  
- Integration tests should do the following:

    - Cover critical application features to ensure that these function work as expected.

    - Include tests for common failure modes 
