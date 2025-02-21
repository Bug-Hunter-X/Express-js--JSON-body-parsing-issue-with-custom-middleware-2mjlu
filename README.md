# Express.js JSON Body Parsing Issue
This repository demonstrates a common issue in Express.js applications where JSON request bodies are not parsed correctly when using custom middleware before `express.json()`.  The issue arises because the custom middleware might not properly handle the request's content type, preventing `express.json()` from parsing the data.

## Bug Description
The `bug.js` file showcases an Express.js application with a custom middleware placed before `express.json()`. This setup causes requests with JSON bodies to result in `req.body` being undefined or empty.

## Solution
The `bugSolution.js` file demonstrates the correct way to handle this.  The custom middleware is either removed or adjusted to not interfere with `express.json()`'s ability to parse the JSON body.