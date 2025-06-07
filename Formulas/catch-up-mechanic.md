---
title: Catch Up Mechanic
description: 
published: true
date: 2025-06-07T14:36:25.747Z
tags: 
editor: markdown
dateCreated: 2025-06-07T14:36:25.747Z
---

## 📖 Catch-Up Mechanic

### Overview

The **Catch-Up Mechanic** is designed to help players who fall behind in land size compete more effectively. It introduces **dynamic discounts** that scale based on how far behind you are compared to the current top player in terms of land.

This system aims to maintain competitiveness and prevent early leads from becoming insurmountable.

---

### 🧮 How It Works

Starting on **Day 2** of the round, players receive discounts if their land is below the land of the current top player.

* **Land Percentage** is calculated as:
  `Your Land / Top Land`
* Based on your land percentage, you receive a **discount**.
* Discounts **scale exponentially** from 0% up to a **maximum of 95%** when you're 25% or more behind.

These discounts apply to:

* 🌍 **Exploration Cost**
* 🏗️ **Building Cost**
* 🛡️ **Defense Cost**

If your land is **very low** compared to the top player, you may receive the **full 95% discount**.

---

### ⚔️ Bonus: Attacked Discount Boost

When you are **attacked**, your current discount is **doubled temporarily (24 ticks)**. This helps you bounce back faster and encourages continued competition.

---

### ⏳ Time-Based Scaling

The mechanic doesn't apply immediately. Instead:

* It **activates on Day 2** of the round.
* It **scales up gradually over 5 days**, reaching full effectiveness by **Day 7**.
* Until then, discounts are **proportionally smaller** and increase with each tick.

---

### 📊 Discount Table Example

| Your Land | % of Top Land | Discount |
| --------- | ------------- | -------- |
| 4750      | 95%           | 0.44%    |
| 4000      | 80%           | 7.00%    |
| 3000      | 60%           | 28.00%   |
| 2000      | 40%           | 63.00%   |
| 1250      | 25%           | 95.00%   |
| 500       | 10%           | 95.00%   |

> **Note:** Discounts are capped at **95%**.

---

### 🧮 Discount Formula

The discount is calculated based on your land relative to the top land, using the following formula:

```
discount =  1.75 * (1 - land_ratio)^2 
```

Where:

* `land_ratio = your_land / top_land`
* `discount` is a value between 0 and 0.95 (i.e. up to 95%)


💡 **Note:**
If your land is at or below 25% of top land, you'll receive the **full maximum discount** of 95%.

---

### ✅ Summary

* Catch-Up Mechanic activates **Day 2**
* Discounts ramp up to full power by **Day 7**
* Applies to **exploring**, **building**, and **defense**
* **Doubled** if you’re attacked
* Designed to **keep the game competitive and fair**
