# Lua Nested Table Iteration Issue

This repository demonstrates a subtle issue related to the order of iteration when using `pairs()` with nested tables in Lua.  The `pairs()` function does not guarantee any specific order, which can lead to unexpected behavior if order is crucial for your application.

## The Problem

The `bug.lua` file contains a function `foo` that recursively iterates over a nested table.  Because `pairs()` doesn't guarantee iteration order, the order of processing nested tables might not be consistent across different Lua implementations or versions.

## The Solution

The `bugSolution.lua` file provides a solution using a custom iterative function that maintains order by explicitly using a sorted keys approach.  This ensures consistent and predictable iteration, avoiding the potential issue arising from `pairs()`'s unordered nature.  This solution demonstrates a more robust approach to iterating through nested tables when order matters.