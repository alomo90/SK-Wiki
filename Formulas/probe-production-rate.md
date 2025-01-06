---
title: Probe Production Rate
description: Explains the Probe Production Rate
published: true
date: 2025-01-05T20:24:50.255Z
tags: 
editor: markdown
dateCreated: 2024-07-28T19:02:13.886Z
---

# Probe Production Rate
Probe Factories produce 0.75 each tick.

From the round of August 2024, a probe production slowdown mechanism is in place to slow down probe bombs.

**TLDR**: If you are above 20 probes / land, you will start producing probes at a slower rate.

![probes_before_after.png](/probes_before_after.png)

What this mechanism does is slow down the production of probes once probes per land reach 20 probes per land. 

20 Probes per land is already a very high number, above max probe defense and above max mining gold. A high probes kingdom will not at all feel the impact of this change. 

This change will help curb probe griefers, although it does not fully solve the problem. 

![probe_production_rate.png](/probe_production_rate.png)
  
The decrease factor is calculated as per the below:
```python
def probe_production_slowdown_factor(probes_per_land: float) -> float:
    TARGET_PROBES_PER_LAND = 20
    MAX_DECREASE_FACTOR = 0.75

    decrease_factor: float = (probes_per_land - TARGET_PROBES_PER_LAND)**2 / 500

    return min(decrease_factor, MAX_DECREASE_FACTOR)
```




