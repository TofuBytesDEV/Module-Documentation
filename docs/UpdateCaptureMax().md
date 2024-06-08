---
title: UpdateCaptureMax()
layout: default

parent: Modifying the Campaign
---
<h2>UpdateCaptureMax(planetName,successfulCaptureMax)</h2>

{: .note }
If you have an active campaign, this function is useful when adjusting only the threshold.

UpdateCaptureMax() allows the Game Master or developers to update the threshold of completed missions for a planet to succeed in its campaign. The function can be called from inside of the game management script and also called live from the in-game developer console as long as the `require(id)` variable is identified with the function.

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| planetName `required` | String     | The name of the planet that will be updated. |
| successfulCaptureMax `required`     | Integer        | The threshold number of completed missions for a planet to succeed in its campaign. |

<h3>Example</h3>

This code will update the planet Utao to succeed after reaching 200,000 successful missions.

```lua
local campaignModule = require(17541574273)
campaignModule.UpdateCaptureMax("Utao",200000)
```
