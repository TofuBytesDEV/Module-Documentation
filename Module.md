---
title: Planet Data
layout: default
---

<h1>Planet Data</h1>

Planets within the game run off of this data table, each time a new value is added, the datastore referencing this must also account for the new value.

```Lua
data = {
planetName = planetName,
active = false,
campaignType = 0,
planetPlaceID = planetPlaceIDs[planetName],
defenseTimer = 0,
factionID = 0
}
```

