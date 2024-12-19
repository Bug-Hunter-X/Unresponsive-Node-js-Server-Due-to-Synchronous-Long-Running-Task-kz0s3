# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler causes the server to become unresponsive.  The `bug.js` file contains the problematic code.  The solution is shown in `bugSolution.js`.

## Problem

The server uses a `while` loop to simulate a task that takes 5 seconds. This blocks the event loop, preventing other requests from being processed.  As a result, the server becomes unresponsive.