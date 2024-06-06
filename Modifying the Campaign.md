---
title: Modifying the Campaign
layout: default
---
{: .note }
These functions are still in development and parameters will change without notice.

<h2>UpdateCampaign(planetName,activeStatus,campaignType,resetProgress,defendDate,factionID)</h2>

UpdateCampaign() allows for the Game Master or developers to perform modifications to the current campaign. The function can be called from inside of the game management script and also called live from the in-game developer console as long as the `require(id)` variable is identified with the function.

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| planetName `required` | String     | The name of the planet that will be updated. |
| activeStatus `required`   | Boolean    | The status on whether players have access to the planet. This will also determine whether it is highlighted on the galactic map or not. `true` or `false` |
| campaignType `required`   | Int        | The current type of campaign of the planet. `0` = not active, `1` = offense, `2` = defend |
| resetProgress `required`  | Boolean    | Determines whether the progression of the planet should be reset back to 0%. `true` or `false` |
| defendDate `required`     | Int        | The end date of a defend campaign will be checked by the game. This value uses the epoch time values and must be formatted in Epoch. |
| factionID `required`     | Int        | The ID of the current faction that the planet is associated with. `0` = None, `1` = Earth, `2` = ?, `3` = ? |

<h3>Example</h3>

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdateCampaign("Utao",true,2,false,1716580800)
```

<h2>UpdatePlanetProgression(planetName,rewardedPoints)</h2>

<h3>Example</h3>

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdatePlanetProgression("Utao",10000000)
```
