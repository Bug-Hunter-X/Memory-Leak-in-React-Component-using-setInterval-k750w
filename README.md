# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` within `useEffect` without proper cleanup.  This can lead to memory leaks if the component unmounts before the interval is cleared.

## Bug

The `bug.js` file contains a component that uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component unmounts, resulting in a memory leak. 

## Solution

The `bugSolution.js` file shows the corrected implementation. It uses the return value of `useEffect` to clear the interval when the component unmounts, preventing memory leaks.

## How to Reproduce

1. Clone the repository.
2. Navigate to the directory in your terminal.
3. Run `npm install`
4. Run `npm start`