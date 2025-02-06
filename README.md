# React useEffect Cleanup Function Issue

This repository demonstrates a common issue with React's `useEffect` hook: the cleanup function not executing as expected.  The example showcases a component that updates a counter and logs messages to the console. The cleanup function should ideally log a message indicating cleanup but it might not always work as expected under certain conditions. 

## Problem
The problem lies in how the `useEffect` hook's dependency array is handled.  In this case, the dependency array `[count]` ensures the effect only runs when the `count` changes. However, issues can arise if the component unmounts prematurely or if the effect is re-run too quickly.