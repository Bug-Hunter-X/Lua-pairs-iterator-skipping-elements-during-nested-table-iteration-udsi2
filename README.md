# Lua pairs Iterator Bug

This repository demonstrates a potential bug in Lua's `pairs` iterator when dealing with nested tables that are modified during iteration. The `bug.lua` file contains code that showcases the issue. The `bugSolution.lua` file presents a solution to mitigate the problem. 

## Bug Description

Lua's `pairs` iterator isn't guaranteed to iterate through all elements of a table if the table's structure changes during iteration.  This can lead to unexpected behavior and skipped elements, especially in recursive functions processing nested tables. The provided example demonstrates this scenario.

## Solution

The solution involves creating a copy of the table before iteration to prevent modification during the process. This ensures that all elements are iterated without interruption. 