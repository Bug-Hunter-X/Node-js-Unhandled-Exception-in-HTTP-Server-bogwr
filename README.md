# Node.js Unhandled Exception in HTTP Server

This repository demonstrates a common error in Node.js where unhandled exceptions within an HTTP server's request handler can cause the server to crash without proper error handling and logging.  The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The original code lacks a `try...catch` block to handle potential errors within the request handler.  If an exception is thrown (as in the `/error` route), the server will terminate unexpectedly without informative logging.

## Solution

The solution includes a `try...catch` block to gracefully handle exceptions.  It logs the error to the console and sends an appropriate error response to the client. This prevents the server from crashing and provides useful debugging information.