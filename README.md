# Rice Cooker Simulator Refactoring

## Overview

This repository contains a refactored version of a JavaScript-based Rice Cooker Simulator. The original code was refactored to improve readability, maintainability, and adherence to JavaScript coding standards.

## Changes Made

### Refactored Code
- Transformed the original rice cooker functionality, previously defined as an object, into a `RiceCooker` class for better encapsulation and organization of methods.
- Introduced a `switch` statement to handle user choices within the simulation, replacing multiple `if-else` conditions for better readability.

### Comparison: Before vs After Refactoring

#### Improvements:
- **Code Structure**: Before, the code was structured around an object with methods, making it prone to becoming unwieldy as more functionality was added. After refactoring, a class-based approach provides better organization and maintainability.
- **Readability**: The use of a class with separate methods for different functionalities enhances code readability and understanding.
- **Switch Statement**: Replacing multiple `if-else` statements with a `switch` statement improves code readability and reduces nesting.

#### Vulnerabilities:
- **Blocking Delay**: Both versions contain a potential issue with the `delaySync` method that employs a blocking delay using a while loop, which could negatively impact performance in real-world applications, especially in single-threaded environments like Node.js.
- **Input Validation**: Both versions lack extensive input validation. While the refactored version performs basic checks for valid numerical input, it doesn’t cover edge cases or inputs beyond numerical choices.

## Running the Simulator

To run the Rice Cooker Simulator:

1. Clone this repository.
2. Ensure you have Node.js installed.
3. Install dependencies using `npm install prompt sync`.
4. Run the simulator using `node main.js`.

## Conclusion

The refactoring process improved the code's structure, readability, and maintainability. However, it retained some vulnerabilities related to input validation and the blocking delay method that could be addressed for better performance and robustness in a production environment.

