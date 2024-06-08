---
title: UpdateActiveStatus()
layout: default

parent: Modifying the Campaign
---
<h2>UpdateActiveStatus(planetName,activeStatus)</h2>

{: .warning }
This is an emergency function and should only be used when needed. Refer to `UpdateCampaign()` to automatically enable/disable the planet status after a defend campaign.

UpdateActiveStatus() allows the Game Master or developers to update a planet's active status. The function can be called from inside of the game management script and also called live from the in-game developer console as long as the `require(id)` variable is identified with the function.

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| planetName `required` | String     | The name of the planet that will be updated. |
| activeStatus `required`     | Boolean        | The status on whether players have access to the planet. This will also determine whether it is highlighted on the galactic map or not. `true` or `false` |

<h3>Example</h3>

This code will update the planet Utao to active status to `true` which will enable the supply line.

```lua
local campaignModule = require(17541574273)
campaignModule.UpdateActiveStatus("Utao",true)
```
