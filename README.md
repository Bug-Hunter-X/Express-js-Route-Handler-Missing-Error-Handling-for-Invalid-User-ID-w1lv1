# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer but doesn't handle cases where the ID is not a number, potentially leading to application crashes or unexpected behavior.

The `bug.js` file contains the erroneous code.  The `bugSolution.js` file provides a corrected version with proper error handling.

## How to reproduce the bug

1. Clone this repository.
2. Run `npm install express`.
3. Run `node bug.js`.
4. Send a GET request to `/users/abc` (or any non-numeric ID).  The application will likely crash or return an unexpected error.

## How to fix the bug

Refer to `bugSolution.js` for the corrected code.  The solution includes error handling to gracefully manage non-numeric IDs, returning appropriate HTTP status codes (e.g., 400 Bad Request) and providing informative error messages.