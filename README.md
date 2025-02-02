# React Router v6 Route Matching Issue

This repository demonstrates a common issue encountered when using nested routes in React Router v6: a more specific route is not matched because a less specific route is defined above it in the Route order. 

The `bug.js` file shows the problematic code, where the `/users/:id` route will never be reached because the `/about` route, which is less specific, matches any path beginning with `/about`. The `bugSolution.js` demonstrates the correct approach to resolve this.  Readme carefully and follow instruction to fix the error.

## Steps to reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server.
4. Navigate to `/about` and `/users/1`. You should see the `About` component rendered both times. This is the error scenario.
5. Then open `bugSolution.js` and compare both files and run the solution file to see the correct routing.

## Solution

The correct approach is to ensure that more specific routes are always defined before less specific routes. See the `bugSolution.js` file for the corrected code.