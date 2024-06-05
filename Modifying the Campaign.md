---
title: Modifying the Campaign
layout: default
---

<h2>UpdateCampaign(planetName,activeStatus,campaignType,resetProgress,defendDate)</h2>

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdateCampaign("Utao",true,2,false,1716580800)

--0 = not active, 1 = offensive, 2 = defensive
```

<h2>UpdatePlanetProgression(planetName,rewardedPoints)</h2>

```Lua
local campaignModule = require(17541574273)
campaignModule.UpdatePlanetProgression("Utao",10000000)
```
