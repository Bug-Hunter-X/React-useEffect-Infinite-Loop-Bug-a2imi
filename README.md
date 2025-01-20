# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by improperly using the `useEffect` hook. The bug occurs when the state update within `useEffect` depends on the previous state value, creating a continuous loop.

## Bug Description
The `MyComponent` attempts to increment a counter using `useEffect` with an empty dependency array ([]).  This means the effect runs only once after the initial render. However, the effect itself modifies the `count` state, causing another re-render, which triggers the effect again, ad infinitum.