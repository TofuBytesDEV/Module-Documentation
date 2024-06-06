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
| defendDate `required`     | Int        | The end date and time of a defend campaign. This value is only referenced when `campaignType = 2` and uses the Int as an Unix time value. As such, time must be converted into in Unix. |
| factionID `required`     | Int        | The ID of the current faction that the planet is associated with. `0` = None, `1` = Earth, `2` = ?, `3` = ? |

<h3>Example</h3>

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdateCampaign("Utao",true,2,false,1716580800)
```

<h2>UpdatePlanetProgression(planetName,rewardedPoints)</h2>

UpdatePlanetProgression() allows for the Game Master or developers to increase or decrease the current progression points of a planet. The function is typically called inside of planet mission scripts but can also be called live from the in-game developer console as long as the `require(id)` variable is identified with the function.

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| planetName `required` | String     | The name of the planet that will be updated. |
| rewardedPoints `required` | Int | The number of points that will be increased or decreased from the existing total.

<h3>Examples</h3>

<h5>Increasing Points</h5>
We are increasing the current progression value for the planet `Utao` by `1000` points.

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdatePlanetProgression("Utao",1000)
```

<h5>Decreasing Points</h5>
We are decreasing the current progression value for the planet `Utao` by `-1000` points.

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdatePlanetProgression("Utao",-1000)
```
