# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: creating an infinite loop within the `useEffect` hook. The bug is caused by the incorrect usage of the `setCount` function inside the `useEffect`'s dependency array.  This leads to the effect running continuously, causing performance issues and potentially crashing the application.

## Bug Description
The `useEffect` hook is designed to perform side effects based on changes to specified dependencies. However, if the effect modifies a dependency that's listed in the dependency array, it creates an endless loop.  In this case, changing `count` triggers the `useEffect` again and again, and continues until the application crashes.