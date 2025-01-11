# React Native useState with Objects - Unexpected Re-render Issue

This repository demonstrates a common issue in React Native applications involving the `useState` hook and object updates.  When updating only a part of an object within the `useState` hook, the component may fail to re-render as expected due to React's shallow comparison mechanism.

The `bug.js` file showcases the problematic code, while `bugSolution.js` offers the corrected implementation. The issue arises because directly modifying the object's property using the spread syntax creates a new object with the same reference.  Therefore, React does not detect any state change.