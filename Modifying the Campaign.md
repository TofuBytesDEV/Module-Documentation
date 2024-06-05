---
title: Modifying the Campaign
layout: default
---

<h3>UpdateCampaign(planetName,activeStatus,campaignType,resetProgress,defendDate)</h3>
| Parameters     | Value Type |
|:---------------|:-----------|
| planetName     | String     |
| activeStatus   | Boolean    |
| campaignType   | Int        |
| resetProgress  | Boolean    |
| defendDate     | Int        |

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdateCampaign("Utao",true,2,false,1716580800)

--0 = not active, 1 = offensive, 2 = defensive
```

<h3>UpdatePlanetProgression(planetName,rewardedPoints)</h3>

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdatePlanetProgression("Utao",10000000)
```
