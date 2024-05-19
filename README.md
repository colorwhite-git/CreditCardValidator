# CreditCardValidator

## Project Description

The **CreditCardValidator** project is designed to automate the verification of credit card numbers using functions and loops, streamlining the process and reducing manual errors. This repository includes scripts to validate multiple credit cards efficiently, saving time and increasing accuracy for clerks.

## Project Requirements

### Starter Code

The starter code includes 15 arrays that each contain the digits of separate credit card numbers. These arrays are prefixed to reflect their status:
- `valid` arrays contain valid credit card numbers.
- `invalid` arrays contain invalid credit card numbers.
- `mystery` arrays can contain either valid or invalid numbers.

All provided credit card arrays are stored in a single array called `batch`.

### Functions to Implement

1. **validateCred()**

    This function checks if a credit card number is valid according to the Luhn algorithm. It should take an array of digits as input and return `true` if the number is valid and `false` otherwise. The original array should not be mutated.

    Steps for the Luhn algorithm:
    - Starting from the farthest digit to the right (check digit), iterate to the left.
    - Double every other digit (excluding the check digit). If doubling results in a number greater than 9, subtract 9 from the result.
    - Sum all the digits.
    - If the sum modulo 10 is 0, the number is valid.

2. **findInvalidCards()**

    This function takes a nested array of credit card numbers and returns a nested array of invalid credit card numbers. It should loop through the array and use `validateCred()` to check each number, keeping track of the invalid ones.

3. **idInvalidCardCompanies()**

    This function identifies the credit card companies that have issued invalid numbers. It takes a nested array of invalid numbers and returns an array of companies that have issued these faulty numbers. The array should not contain duplicates.

    Accepted companies:
    - Amex (American Express) starts with 3
    - Visa starts with 4
    - Mastercard starts with 5
    - Discover starts with 6

    If the first digit of a number does not match any of these, print "Company not found".

## Project Extensions

1. Use credit card numbers from a credit card number generator and validator site to test the functions.
2. Create a function to convert a string of credit card numbers into an array of digits.
3. Create a function to convert invalid credit card numbers into valid numbers.