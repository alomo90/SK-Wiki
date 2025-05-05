---
title: Probe Losses
description: 
published: true
date: 2025-05-05T05:26:50.361Z
tags: 
editor: markdown
dateCreated: 2024-07-27T10:03:24.513Z
---

# Probes Losses

## Calculating Probe Losses

Up until round 76, base probe losses were 1.1% to 2.2%, calculated as 1.1% + random(1.1%).
From round 76 onwards, the amount of randomness is reduced, but the save average probe losses are maintained.   
  
The average probe loss used to be 1.1 + (1.1 / 2) = 1.65%. Which is the same as 1.1 * 1.5 = 1.65%.
So instead of starting from 1.1 and adding a random 1.1, we now start from 1.65, making it more centered.  
  
To keep the full amount of randomness, we'd have use -0.5 * Random and + 0.5 * Random.
We're reducing the randomness, so we're using -0.25 * Random and + 0.25 * Random.
```
@ProbeLossPercentage = @BASE_PROBE_LOSSES * (1.5 - 0.25 * dbo.RandomNumber() + 0.25 * dbo.RandomNumber())
```
Aggressive Probe missions, such as robs and sabos the probe losses are 50% higher.
```
SET @ProbeLossFactor = @ProbeLossFactor * @MissionTypeFactor
```

Fails double losses. Shields reduce losses by 50%, and so does probe armour. They are multiplicative.  
```
@FAIL_FACTOR real = 2.0,
@SHIELDED_FACTOR real = 0.5,
@PROBE_ARMOUR_FACTOR real = 0.5,

IF (@Success = 0) SET @ProbeLossFactor = @ProbeLossFactor * @FAIL_FACTOR
IF (@IsShielded > 0) SET @ProbeLossFactor = @ProbeLossFactor * @SHIELDED_FACTOR
IF (@ProbeArmour = 1) SET @ProbeLossFactor = @ProbeLossFactor * @PROBE_ARMOUR_FACTOR
```

All other probe loss factors are additive.

## An Example
Robbing, 10k probes, shielded, probe armour, fail, shadow 1 (-10% losses)

base loss = 1.1

Calculating randomized loss
Loss = 1.1 * (1.5 - 0.25 * Random + 0.25 * Random) 
Loss = 1.65 + random - random

Aggressive Probing
Loss = 1.65 + 50% = 2.475

Shielded
Loss = 2.475 * 0.5 = 1.2375

Probe Armour
Loss = 1.2375 * 0.5 = 0.61875

Fail
Loss = 0.61875 * 2 = 1.2375

Shadow 1
Loss = 1.2375 - 0.1 = 1.11375

Probe Loss = 1.11375% * 10'000 = 111 probes
