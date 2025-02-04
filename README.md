# Unhandled Exception in Express.js POST Route

This repository demonstrates a common error in Express.js applications: unhandled exceptions caused by missing or malformed request bodies in POST requests.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version with robust error handling.

## Bug Description

The original code attempts to access properties from the request body (`req.body`) without checking if these properties exist. If a request is made without the expected data, or with malformed JSON, the application crashes with an `undefined` error.

## Solution

The solution includes comprehensive error handling. It checks for the existence of necessary properties in `req.body` before accessing them.  If the request body is invalid or missing, an appropriate error response is returned to the client.