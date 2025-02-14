# React 19 useEffect Cleanup for setInterval
This repository demonstrates a common error in React 19 involving the improper use of `setInterval` within the `useEffect` hook, which can lead to memory leaks.  The solution shows how to correctly use `setInterval` by providing a cleanup function.

## Bug
The `bug.js` file showcases the incorrect implementation.  The `setInterval` is started, but there's no mechanism to stop it when the component unmounts. This results in the interval continuing to run indefinitely, consuming resources and leading to potential memory leaks.

## Solution
The `bugSolution.js` file presents the corrected implementation.  The `useEffect` hook now returns a cleanup function that uses `clearInterval` to stop the interval when the component unmounts. This prevents the memory leak.

## How to Run
1. Clone the repository
2. Navigate to the repository directory in your terminal
3. Run `npm install`
4. Run `npm start`