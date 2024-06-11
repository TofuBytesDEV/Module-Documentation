---
title: SetMajorObjectivePlanets()
layout: default

parent: Understanding Major Objectives
---
<h2>SetMajorObjectivePlanets(planetList)</h2>

SetMajorObjectivePlanets() allows the Game Master or developers to update the list of planets in the active major objective. The function can be called from inside of the game management script and also called live from the in-game developer console as long as the `require(id)` variable is identified with the function.

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| planetList `required` | Table     | A table of planet names. |

<h3>Returns</h3>

| Variable     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| Status | Boolean     | `true` or `false` |

<h3>Examples</h3>

<h5>Updating the Planets</h5>
This code will update the major objective list of planets.

```lua
local Module = require(17541574273)
local planetList = {"Utao"}
Module.SetMajorObjectivePlanets(planetList)
```
