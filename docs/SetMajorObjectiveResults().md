---
title: SetMajorObjectiveResults()
layout: default

parent: Understanding Major Objectives
---
<h2>SetMajorObjectiveResults(winMessage,failMessage)</h2>

SetMajorObjectiveResults() allows the Game Master or developers to update the results posted at the end of a major objective. The function can be called from inside of the game management script and also called live from the in-game developer console as long as the `require(id)` variable is identified with the function.

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| winMessage `required` | String     | Message when the major objective succeeds. |
| failMessage `required` | String     | Message when the major objective fails. |

<h3>Examples</h3>

<h5>Updating the Results</h5>

```lua
local campaignModule = require(17541574273)
local winMessage = "Congrats, you wont!"
local failMessage = "We failed!"
campaignModule.SetMajorObjectiveResults(winMessage,failMessage)
```
