# React useEffect Hook Performance Issue

This repository demonstrates a common performance issue in React applications involving the `useEffect` hook. The provided code snippet shows an example where the `useEffect` hook is called on every render, leading to unnecessary re-renders and potentially impacting application performance.

## Bug Description
The `useEffect` hook's dependency array `[count]` is missing, causing the effect to run on every render of the component, even when the `count` value hasn't changed.  This results in excessive logging and unnecessary computations.

## Solution
The solution involves correctly defining the dependency array. By specifying `[count]` as the dependency array, useEffect will only execute when `count` changes.