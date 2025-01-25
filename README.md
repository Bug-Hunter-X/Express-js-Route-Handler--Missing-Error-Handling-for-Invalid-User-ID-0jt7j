# Express.js Route Handler: Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user input. Specifically, this example showcases a route that fetches a user by ID but fails to handle cases where the provided ID is not a valid number.

## Bug Description

The `bug.js` file contains an Express.js route handler that retrieves a user based on their ID.  It attempts to parse the ID as an integer using `parseInt()`, but it doesn't include any error handling if the ID is not a number. This can lead to unexpected behavior or application crashes.

## Solution

The `bugSolution.js` file provides a corrected version of the route handler. It includes error handling to gracefully manage cases where the user ID is invalid. The solution involves checking if `parseInt(userId)` returns `NaN` before proceeding.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `npm install` to install the necessary dependencies.
4. Run `node bug.js` and try accessing the route with a non-numeric ID (e.g., `/users/abc`). Observe the error.
5. Run `node bugSolution.js` and try accessing the route with the same non-numeric ID. Observe the improved error handling.