---
title: Building Costs
description: How Building Costs are calculated
published: true
date: 2025-01-05T20:24:47.056Z
tags: formulas
editor: markdown
dateCreated: 2025-01-04T13:30:06.701Z
---

# Calculating Building Costs
```SQL
@BuildingCostBaseFactor real = 56.9241

@Bonus = 1 
	+ @PlanetBonus 
	+ @RaceFactor  
	+ @StateDiscount
	+ @ModuleDiscount 
	+ @AllianceBonus  
	+ @EventDiscount

@BuildingCost = (1 - @Bonus) * @BuildingCostBaseFactor * SQRT(@Land)
```