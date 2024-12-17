# Infinite Re-renders in React useEffect Hook

This repository demonstrates a common issue in React applications: infinite re-renders caused by a missing dependency in the `useEffect` hook.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides the corrected version.

## Problem

The `useEffect` hook in `bug.js` lacks the `count` variable as a dependency.  This leads to an infinite loop because the effect runs on every render, causing the component to re-render, triggering the effect again, and so on.

## Solution

The `bugSolution.js` file shows the correct implementation.  By adding `count` to the dependency array, the effect only runs when the value of `count` changes, resolving the infinite re-render issue. 

## How to reproduce
1. Clone the repo
2. run `npm install`
3. run `npm start`
