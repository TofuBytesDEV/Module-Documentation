---
title: GetMajorObjectiveResults()
layout: default

parent: Understanding Major Objectives
---
<h2>GetMajorObjectiveResults()</h2>

Returns a table of results in the major objective.

<h3>Returns</h3>

| Variable     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| resultsList | Table     | Returns a table of results in the major objective. |

<h3>Examples</h3>

This code will print the win and fail messages in the major objective.

```lua
local Module = require(17541574273)
local resultsList = Module.GetMajorObjectivePlanets()

for -,v in pairs(resultsList) do
print(v)
```
