# Uncommon React useEffect Infinite Loop Bug
This repository demonstrates a subtle bug involving React's `useEffect` hook that can lead to an infinite loop and excessive console logging. The issue arises from an incorrect or missing dependency array, causing the effect to run after every render, instead of only when specific dependencies change.

## Bug Description
The provided `MyComponent` uses `useEffect` to log the current count to the console. However, the effect lacks a dependency array or includes incorrect dependencies, leading to an infinite loop.  Each render updates the count which triggers the effect to run again, resulting in a never-ending cycle. 

## Solution
To solve the issue, the dependency array `[count]` must be correctly specified. This ensures that the `useEffect` function only runs when the value of the `count` state variable changes.