# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common bug in React 19 involving an infinite loop within the `useEffect` hook.  The bug arises from improper dependency handling within the `useEffect`'s dependency array, causing it to re-run endlessly. This example shows the problem and its solution.

## Bug Description

The `useEffect` hook is designed to perform side effects based on changes to specified dependencies. However, if the dependencies are not correctly specified, it can lead to an infinite loop, causing performance degradation and, potentially, a crash.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console output and the continuous re-rendering of the component, causing performance issues.  

## Solution

The solution involves carefully specifying the dependencies in the `useEffect`'s dependency array. In this case, we include `count` as a dependency so that the effect only runs when `count` changes.
