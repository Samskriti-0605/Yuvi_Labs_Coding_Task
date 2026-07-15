# 2D Even Number Highlighter

## Problem Statement
Design and implement a Java program that generates a **P × P** two-dimensional array populated with random even numbers ranging from **2 to 16**. The program should allow the user to enter an even number, search for that value throughout the array, highlight every occurrence of the selected number, and display the total number of times it appears. The solution should also validate user inputs to ensure the program handles invalid entries appropriately.

## Solution Overview
This program demonstrates the use of two-dimensional arrays, methods, nested loops, random number generation, and input validation in Java. It creates a square matrix based on the size entered by the user and fills each position with a randomly generated even number between **2** and **16**.

The generated array is displayed in a well-formatted table with row and column indices for better readability. The user is then prompted to enter an even number within the valid range. After validating the input, the program searches the entire array, highlights every matching value, and displays the total number of occurrences.

## How the Code Works

### Step 1: Accept User Input
The program asks the user to enter the size of the square array. It validates that the input is a positive integer before proceeding. If the input is invalid, the program terminates with an appropriate message.
The program then asks the user to enter an even number between **2** and **16**. This input is also validated to ensure it is an even integer within the specified range.

### Step 2: Create the Array
A two-dimensional integer array of size **P × P** is created using the user-provided size.
```java
int[][] array = new int[size][size];
```

### Step 3: Generate Random Even Numbers
Each element of the array is assigned a random even number between **2** and **16**.
```java
array[i][j] = (random.nextInt(8) + 1) * 2;
```
This expression generates values from **1** to **8** and multiplies them by **2**, ensuring that only even numbers are stored.

### Step 4: Display the Array
The `Yuvi_Labs()` method is responsible for displaying the matrix in a structured table. It prints row and column indices, making the output easy to understand.
Initially, the array is displayed without any highlighted values.

### Step 5: Search for the Selected Number
Using nested loops, the program traverses every element of the matrix.
For each element:
- It compares the current value with the user's selected number.
- If both values match, the occurrence counter is incremented.
This ensures that every element in the array is checked exactly once.

### Step 6: Highlight Matching Values
After counting the occurrences, the array is displayed again using the same display method.
Whenever the selected number is encountered, it is enclosed within square brackets, making it visually distinguishable from the other values.

### Step 7: Display the Result
Finally, the program prints the total number of times the selected even number appears in the generated array.

## Output Explanation
The program produces the output in three stages:
1. A randomly generated **P × P** array containing even numbers between **2** and **16**.
2. The same array with all occurrences of the selected number highlighted using square brackets.
3. The total count of how many times the selected number appears.
Since the array values are generated randomly, every execution produces a different arrangement of numbers. As a result, both the highlighted positions and the occurrence count vary with each run.

## Features
- Accepts a user-defined array size.
- Generates a random **P × P** array.
- Uses only even numbers between **2** and **16**.
- Validates all user inputs.
- Displays the array in a readable tabular format.
- Highlights all matching values.
- Counts and displays the total occurrences of the selected number.
- Uses a separate method for displaying the array, improving code readability and reusability.

## Concepts Used
- Two-Dimensional Arrays
- Methods
- Nested Loops
- Conditional Statements
- Random Number Generation
- Scanner for User Input
- Input Validation
- Console Formatting
- Matrix Traversal
