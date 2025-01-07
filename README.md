# Asynchronous Update in React's useState Hook

This repository demonstrates a common pitfall when working with the `useState` hook in React 19 (and earlier versions).

Because `setCount` is asynchronous, the value of `count` is not updated instantly. Logging it immediately after calling `setCount` will result in the *previous* state being logged, potentially leading to unexpected behavior and difficult-to-debug issues. 

**The Bug:** The example shows how directly accessing `count` after calling `setCount` will not reflect the update. The solution demonstrates using useEffect with the `count` value as a dependency to log the updated value after the state has changed.   