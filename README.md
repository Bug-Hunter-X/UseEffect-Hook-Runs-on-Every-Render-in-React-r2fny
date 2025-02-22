# React useEffect Hook Bug

This repository demonstrates a common bug in React's `useEffect` hook where it runs on every render instead of only when its dependencies change. This can lead to performance problems and unexpected behavior.

## The Bug

The `useEffect` hook in `bug.js` is designed to log the current count whenever it changes.  However, due to a missing dependency array, it actually runs on every render, causing unnecessary logging and potential performance overhead.

## The Solution

The `bugSolution.js` file corrects this issue by including the `count` variable in the dependency array.  This ensures that the `useEffect` hook only runs when the `count` value changes. 

## How to Reproduce

1. Clone this repository.
2. Open `bug.js` and observe the console logs every time the component renders. 
3. Open `bugSolution.js` and compare the behavior. The console logs only when the counter value is changed.

## Related Resources

* [React's useEffect Hook Documentation](https://reactjs.org/docs/hooks-reference.html#useeffect)