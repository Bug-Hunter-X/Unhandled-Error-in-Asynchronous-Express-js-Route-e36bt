# Unhandled Error in Asynchronous Express.js Route

This repository demonstrates a common error in Node.js Express.js applications: unhandled errors within asynchronous operations.  The `bug.js` file showcases a scenario where an asynchronous route handler throws an error, causing the server to crash without proper logging or error handling. The `bugSolution.js` file demonstrates a corrected version with proper error handling using a `try...catch` block.

## Bug

The bug lies in the lack of error handling within the asynchronous operation in the `/` route.  If the random number generated is greater than or equal to 0.5, an error is thrown, leading to a server crash.  There's no mechanism to catch this error, log it, or send a graceful response to the client.

## Solution

The solution involves using a `try...catch` block to handle potential errors. This ensures that the error is caught, logged (for debugging), and a proper response is returned to the client, preventing a server crash.
