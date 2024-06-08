---
title: UpdatePlanetProgression()
layout: default

has_children: true
---
<h2>UpdatePlanetProgression(planetName,rewardedPoints)</h2>

UpdatePlanetProgression() allows the Game Master or developers to increase or decrease the current progression points of a planet. The function is typically called inside of planet mission scripts but can also be called live from the in-game developer console as long as the `require(id)` variable is identified with the function.

| Parameters     | Value Type | Use          |
|:---------------|:-----------|:-------------|
| planetName `required` | String     | The name of the planet that will be updated. |
| rewardedPoints `required` | Integer | The number of points that will be increased or decreased from the existing total.

<h3>Examples</h3>

<h5>Increasing Points</h5>
This code will increase the current progression value for the planet Utao by 1,000 points.

```lua
local campaignModule = require(17541574273)
campaignModule.UpdatePlanetProgression("Utao",1000)
```

<h5>Decreasing Points</h5>
This code will decrease the current progression value for the planet Utao by 1,000 points.

```lua
local campaignModule = require(17541574273)
campaignModule.UpdatePlanetProgression("Utao",-1000)
```
