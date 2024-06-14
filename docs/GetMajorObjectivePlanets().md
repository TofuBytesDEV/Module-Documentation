---
title: GetMajorObjectivePlanets()
layout: default

parent: Understanding Major Objectives
---
<h2>GetMajorObjectivePlanets()</h2>

Returns a table of planets in the major objective.

<h3>Returns</h3>

| Variable     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| planetList | Table     | Returns a table of all planets in the major objective. |

<h3>Examples</h3>

This code will print each planet in the major objective.

```lua
local Module = require(17541574273)
local planetList = Module.GetMajorObjectivePlanets()

for -,v in pairs(planetList) do
print(v.." is a part of the major objective.")
end
```
