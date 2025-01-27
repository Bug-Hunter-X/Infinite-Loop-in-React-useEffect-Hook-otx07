# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The component enters an infinite loop due to a missing dependency in the `useEffect` hook's dependency array.

## Bug Description

The `useEffect` hook, without proper dependencies, triggers on every render. This leads to an infinite loop where the component continuously updates the state and causes the effect to run again, and so on.

## Solution

The solution involves correctly specifying the dependencies in the `useEffect` hook's dependency array.  The dependency array should include any state variables or props that the effect relies upon.  In this case, the 'count' state variable is the dependency that triggers the effect when it changes.