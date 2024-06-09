---
title: AnnounceMajorObjective()
layout: default

parent: Modifying the Campaign
---
<h2>AnnounceMajorObjective(Body,Objective,Time)</h2>

UpdateMajorObjective() allows the Game Master or developers to update the text for a major objective. The function is typically called inside of planet mission scripts but can also be called live from the in-game developer console as long as the `require(id)` variable is identified with the function.

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| Body `required` | String     | The body of the major objective. |
| Objective `required` | String | The task(s) of the major objective. |
| Time `required` | Int | The end time of the major objective. It must be in Unix format. |

<h3>Examples</h3>

<h5>Updating the Major Objective</h5>
This code will update the major order to inform players of a birthday and to wish them a happy birthday, with a timer of June 8, 2024 at 12:00 AM PDT.

```lua
local Module = require(17785084930)
Module.AnnounceMajorObjective("Today is a birthday!","Say Happy Birthday",1717830000)
```
