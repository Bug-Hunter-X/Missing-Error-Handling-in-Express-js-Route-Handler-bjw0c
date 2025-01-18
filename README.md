# Express.js Route Handler Error Handling Bug

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  The `bug.js` file contains a route that fetches a user by ID.  However, it doesn't handle cases where the ID is not a valid integer, potentially leading to errors or unexpected behavior.  The `bugSolution.js` file provides a corrected version with proper error handling.

## How to Reproduce

1. Clone this repository.
2. Run `npm install express`
3. Run `node bug.js`
4. Try accessing `/users/abc` or `/users/12345` (assuming no user with such ID exists).

## Solution

The solution involves adding error handling to check if the `userId` can be parsed as an integer and handling the case where the user is not found more gracefully.