# React 19 useEffect Bug

This repository demonstrates a potential issue with `useEffect` in React 19 where the effect runs after every render, even when a dependency array is provided. This can lead to performance problems if not handled correctly.

## Bug Description

The `useEffect` hook is supposed to run only when its dependencies change.  However, in this case, the effect runs on every render, which is inefficient.

## Solution

The issue arises from the effect function accessing the `count` variable without using it in the dependency array.  The solution is to use a dependency array correctly.