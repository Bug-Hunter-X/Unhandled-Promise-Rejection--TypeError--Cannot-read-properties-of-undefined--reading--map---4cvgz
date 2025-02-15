# React Native: Accessing State Before Initialization

This repository demonstrates a common error in React Native: attempting to access a state variable before it has been initialized using the `useState` hook.  The error typically manifests as a `TypeError: Cannot read properties of undefined (reading 'map')` or a similar error related to accessing a property of `undefined`.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected implementation.  The issue arises from trying to use the state variable before React has had a chance to assign it a value in the initial render.

## How to reproduce:
1. Clone the repository.
2. Run `npm install` to install the dependencies.
3. Run the application using your preferred React Native method (e.g., `npx react-native run-android` or `npx react-native run-ios`).
4. Observe the error message in the console.  Try to solve this error.

## Solution:
The solution involves ensuring the state variable is properly initialized and accessed only after it has a defined value.  Conditional rendering or using the `useEffect` hook to run the state-dependent logic after the first render are common solutions.
