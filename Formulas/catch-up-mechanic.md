---
title: Catch Up Mechanic
description: 
published: true
date: 2025-07-02T07:46:56.604Z
tags: 
editor: markdown
dateCreated: 2025-06-07T14:36:25.747Z
---

## 📖 Catch-Up Mechanic

### Overview

The **Catch-Up Mechanic** helps players who fall behind in land size remain competitive. It introduces **dynamic, scaling discounts** based on how far behind you are compared to the **Top 15 Land Average**.

---

### 🧮 How It Works

Starting on **Day 2** of the round, players whose land is below the **Top 15 Land Average** receive discounts on key actions.

* **Land Percentage** is calculated as:  
  `Your Land / Top 15 Land Average`
* Discounts scale based on how far behind you are.
* Discounts are **multiplicative**, meaning they stack with other effects proportionally.

Discounts apply to:

* 🌍 **Exploration Costs**
* 🏗️ **Building Costs**
* 🛡️ **Defense Costs**

---

### ⚔️ Attacked Discount Boost

When attacked, players receive a temporary **bonus discount**:

* Each attack activates an extra **24%** of your current discount.
* The bonus **decays over time**, reducing by **0.5% per tick**.
* if you were at 50% bonus, your discount rises to 62% (24% more) 

---

### ⏳ Time-Based Scaling

* Catch-Up begins on **Day 2**
* The effect **scales gradually** over 5 days, reaching full power by **Day 7**

---

### 📊 Discount Table Example

| Your Land | % of Top 15 Avg Land | Discount |
| --------- | --------------------- | -------- |
| 4750      | 95%                   | 0.31%    |
| 4000      | 80%                   | 5.00%    |
| 3000      | 60%                   | 20.00%   |
| 2000      | 40%                   | 45.00%   |
| 1250      | 25%                   | 70.31%   |
| 500       | 10%                   | 95.00%   |

> **Note:** Discount caps vary by category.

---

### 🧮 Discount Formula

The discount is calculated using:
```
discount = 1.25 * (1 - land_ratio)^2
```


Where:

* `land_ratio = your_land / top_15_land_average`
* Resulting discount is capped based on category.

---

### 🚫 Maximum Discounts

* 🛡️ **Defense**: Max **65%**
* 🌍 **Explore & 🏗️ Building**: Max **95%**

All discounts are **multiplicative**.

---

## 🔁 Round Changes

### July 2025
* Catch-up Factor set to **1.25**, previous **1.75**
* Discounts now based on **Top 15 Land Average**, previously top land
* Each attack triggers a **24%** increase of the discount, previously 100%
* Attack bonuses **decay 0.5% per tick**, previously lasted 24 ticks 
* Defense discount capped at **65%**, previously 95%
* Defense Discounts are now **multiplicative**


