# Unhandled Promise Rejection in Express.js Route Handler

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in route handlers.  The `bug.js` file showcases the problematic code, where a database interaction (simulated here) lacks proper error handling.  The `bugSolution.js` file provides a corrected version with robust error handling. 

## Problem

The original code fails to handle potential errors during database queries or other asynchronous operations within the route handler. If the database query fails, a promise rejection occurs, leading to crashes or unexpected behavior. 

## Solution

The solution introduces comprehensive error handling using `try...catch` blocks or `.catch()` to gracefully manage errors.  This prevents unhandled promise rejections and ensures the application remains stable even during database failures.