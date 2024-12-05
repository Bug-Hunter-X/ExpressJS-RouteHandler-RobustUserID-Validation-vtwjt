# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user input.  Specifically, the example code attempts to parse a user ID from the request parameters as an integer without validating that the input is actually a number. This can lead to unexpected behavior or even crashes if the ID is not a valid integer.

The `bug.js` file contains the flawed code.  The `bugSolution.js` file provides a corrected version that includes robust error handling.

## How to Reproduce the Bug

1. Clone this repository.
2. Run `npm install express` to install the necessary dependency.
3. Run `node bug.js`.
4. Make a request to `/users/<invalid_id>` (e.g., `/users/abc`). You'll likely see an error message. 

## Solution

The solution involves adding validation to ensure the user ID is a valid number before attempting to parse it.  The improved code also includes a more informative error response.