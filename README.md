# React Router Dom v6 Catch-all Route Issue

This repository demonstrates a problem with the catch-all route (`*`) in React Router Dom v6.  The issue occurs when attempting to use a catch-all route to render a '404 Not Found' component.  The expected behavior is that any route not explicitly defined should trigger the catch-all route; however, in this instance, it's not functioning correctly.

The `App.js` file contains the problematic code. The `AppSolution.js` file offers a corrected implementation.  The problem and solution are described below. 

## Problem

The primary problem lies in the order or placement of routes within the Routes component.  The catch-all route needs to be last; otherwise, it might be unintentionally overridden by other routes.

## Solution

The solution is to ensure the catch-all route (`/*`) is placed at the end of the routes array within the `Routes` component. This guarantees that it will only match routes that haven't already been matched by preceding routes. 