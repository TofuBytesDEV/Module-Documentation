---
title: Modifying the Campaign
layout: default
---
{: .note }
These functions are still in development and parameters will change without notice.

<h2>UpdateCampaign(planetName,activeStatus,campaignType,resetProgress,defendDate)</h2>

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| planetName `required` | String     | The name of the planet that will be updated. |
| activeStatus `required`   | Boolean    | The status on whether players have access to the planet. This will also determine whether it is highlighted on the galactic map or not. |
| campaignType `required`   | Int        | Determines what type of campaign or mission types will be available. `0 = not active`, `1 = offense`, `2 = defend` |
| resetProgress `required`  | Boolean    | Determines whether the progression of the planet should be reset back to 0%.|
| defendDate `optional`     | Int        | The end date of a defend campaign will be checked by the game. This value uses the epoch time values and must be formatted in Epoch. |

<h5>Example</h5>

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdateCampaign("Utao",true,2,false,1716580800)
```

<h2>UpdatePlanetProgression(planetName,rewardedPoints)</h2>

<h5>Example</h5>

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdatePlanetProgression("Utao",10000000)
```
