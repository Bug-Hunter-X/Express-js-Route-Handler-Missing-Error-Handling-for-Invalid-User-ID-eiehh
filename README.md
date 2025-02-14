# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, this example shows a route that retrieves a user by ID, but fails to handle cases where the ID is not a valid number.

## Bug

The `bug.js` file contains an Express.js route handler that retrieves a user from an array based on their ID.  If the provided ID is not a number, the `parseInt(userId)` function will return `NaN`, causing the `find` method to always return `undefined`. This will lead to a crash and potential server errors.

## Solution

The `bugSolution.js` file provides a corrected version of the route handler. It includes error handling to gracefully manage non-numeric IDs.  It also checks for the user's existence before sending a response.