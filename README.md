# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js where a long-running operation in a request handler can block the event loop, causing the server to hang and become unresponsive to new requests. The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations to prevent blocking.

## Problem

The original code has a `while` loop that simulates a 5-second delay. During this delay, the server is unable to process other requests, leading to a hang.

## Solution

The solution uses asynchronous operations and timers (`setTimeout`) to handle long-running tasks without blocking the event loop. This allows the server to remain responsive to other requests even while a long task is in progress.