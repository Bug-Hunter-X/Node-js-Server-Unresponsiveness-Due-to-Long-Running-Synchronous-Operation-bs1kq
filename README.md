# Node.js Server Unresponsiveness Bug

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler blocks the event loop, causing the server to become unresponsive.

## Bug Description

The `server.js` file contains a simple HTTP server.  However, the request handler includes a `while` loop that keeps the CPU busy for 5 seconds.  During this time, the server cannot process any other requests, leading to unresponsiveness.

## Solution

The `serverSolution.js` file demonstrates how to fix this by using asynchronous operations or offloading long-running tasks to worker threads or other asynchronous mechanisms. This prevents blocking the event loop and maintains the server's responsiveness.