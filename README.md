# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common error in React's `useEffect` hook: omitting dependencies, leading to unnecessary re-renders. The `bug.js` file contains the problematic code, while `bugSolution.js` provides the corrected version.

## Problem
The original code includes a `useEffect` hook without specifying any dependencies in the second argument (the dependency array). This means the effect runs after every render, not just when the `count` changes. This causes inefficient re-renders and may lead to unexpected behavior or performance issues.

## Solution
The corrected code includes `[count]` in the dependency array. This ensures the `useEffect` hook only runs when the `count` value changes. 