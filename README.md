# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications where a long-running operation in the request handler blocks the event loop, causing the server to become unresponsive.  The `server.js` file contains the problematic code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The primary problem is that the `while` loop in `server.js` keeps the event loop busy for 5 seconds, preventing it from processing other requests or events. This leads to unresponsiveness and poor performance.

## Solution

The solution involves using asynchronous operations to avoid blocking the event loop.  This allows the server to handle other requests concurrently.