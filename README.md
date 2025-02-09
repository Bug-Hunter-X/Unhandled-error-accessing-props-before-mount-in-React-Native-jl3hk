# React Native: Accessing state or props before component mount

This repository demonstrates a common error in React Native where you try to access component state or props before the component has fully mounted.  The example shows how to reproduce the error and the correct way to handle it using lifecycle methods.

## Bug
The `bug.js` file showcases the error. Attempting to access `this.props.initialData` within the constructor results in `this.props` being undefined, causing the error. 

## Solution
The `bugSolution.js` file provides the corrected implementation. Accessing props or state initialization should be done within `componentDidMount` lifecycle method, ensuring that the component has mounted and the props are available.