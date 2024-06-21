---
title: Understanding Supply Lines
layout: default
---

<h2>Understanding Supply Lines</h2>
Each planet has a supply line connecting it to a planet, whether it is Earth or a neighboring planet. These are also routes into different sectors of the galactic frontier. Note that supply lines will only display under the following conditions `active = true` or `factionID = 1`. This allows planet routes that are not captured to no display.

When configuring a planet with a supply line, the planet uses a `Beam` object with two `Attachment` objects. The table below will assist in referencing how to link each `Attachment`.

| Property     | Value Type |
|:---------------|:-----------|
| Attachment0 | Destination - Current Planet |
| Attachment1 | Source - Previous Planet |
