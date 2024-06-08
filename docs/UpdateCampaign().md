---
title: UpdateCampaign()
layout: default
parent: Modifying the Campaign
---

<h2>UpdateCampaign(planetName,activeStatus,campaignType,resetProgress,defendDate,factionID,successfulCaptureMax,setToOffense)</h2>

UpdateCampaign() allows the Game Master or developers to perform modifications to the current campaign. The function can be called from inside of the game management script and also called live from the in-game developer console as long as the `require(id)` variable is identified with the function.

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| planetName `required` | String     | The name of the planet that will be updated. |
| activeStatus `required`   | Boolean    | The status on whether players have access to the planet. This will also determine whether it is highlighted on the galactic map or not. `true` or `false` |
| campaignType `required`   | Integer        | The current type of campaign of the planet. `0` = not active, `1` = offense, `2` = defend |
| resetProgress `required`  | Boolean    | Determines whether the progression of the planet should be reset back to 0%. `true` or `false` |
| defendDate `required`     | Integer        | The end date and time of a defend campaign. This value is only referenced when `campaignType = 2` and uses the Int as an Unix time value. As such, the date and time must be converted into Unix. |
| factionID `required`     | Integer        | The ID of the current faction that the planet is associated with. `0` = None, `1` = Earth, `2` = ?, `3` = ? |
| successfulCaptureMax `required`     | Integer        | The threshold number of completed missions for a planet to succeed in its campaign. |
| setToOffense `required` | Boolean | Determines whether the will become offensive active after a defend campaign. |

<h3>Example</h3>

This code will update the planet Utao to active, defend campaign, and reset the progress with the end date/time of `Wednesday, June 5, 2024 12:00:00 AM`, faction 2, with a success threshold of 500,000.

```lua
local campaignModule = require(17541574273)
campaignModule.UpdateCampaign("Utao",true,2,false,1717570800,2,500000)
```
