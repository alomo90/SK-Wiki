---
title: Offensive Cap
description: 
published: true
date: 2026-06-29T11:54:23.100Z
tags: 
editor: markdown
dateCreated: 2025-04-23T07:24:14.855Z
---

# ⚖️ Anti-Turtle Cap System

The **Anti-Turtle Cap System** controls how much offense you are allowed to make.  

Try out the calculator: [AT Cap Calcualtor](https://docs.google.com/spreadsheets/d/1ePLEIHaT1IKgEZaK8T8U8r0HvEX9XApjXYjbmIrbr7c/edit?usp=sharing)

---

## 📊 Cap Ratio

| Cap Type  | Percentage |
|-----------|------------|
| Defense   | 45%        |
| Offense   | 55%        |

- You can train up to 55% of your cap in **offense**.
- 45% must go into **defensive power**.
- **Flexible units** contribute partially to the defense cap (35%).

---

## 🧱 Unit Roles and Cap Contribution

| Unit Type      | Offense | Defense | Cap Role       | Contribution to Offense Cap |
|----------------|---------|---------|----------------|------------------------------|
| **Troopers**   | 4       | 0       | Pure Offense   | 0                        |
| **Laser Troopers** | 0   | 4       | Pure Defense   | 4                     |
| **Tanks**      | 9       | 9       | Flex           | 3.15         |
| **Soldiers**   | 1       | 1       | Flex           | 0.35         |

---

## 📐 How the Cap Works

1. **Calculate Defense Cap Value**  
   - Full defense value from **pure defensive units**
   - **35%** of defense value from **flex units**

2. **Determine Offense Cap from Defense Cap**  
   - You can train up to a **55:45** ratio of offense to defense.

3. **Apply Caps When Training Units**  
   - The number of **troopers** you can train is based on your current defense value.

---

## ⚔️ Example Calculation

Let’s say your kingdom has:

- 5,000 **Laser Troopers** (0/4)  
- 1,000 **Tanks** (9/9)  
- 1,000 **Soldiers** (1/1)  
- ??? **Troopers** (0/4) — we’ll calculate how many you're allowed

### 🔧 Step 1: Calculate Defense Cap Value

- **Laser Troopers**:  
  5,000 × 4 = **20,000** (100% contribution)

- **Tanks**:  
  1,000 × 9 = 9,000 → 35% = **3,150**

- **Soldiers**:  
  1,000 × 1 = 1,000 → 35% = **350**

#### ✅ Total Defense Cap Value:  
**20,000 + 3,150 + 350 = 23,500**

---
### 💥 Step 2: Calculate Max Offense (Troopers Allowed)

Using the 55:45 cap ratio:

Trooper Offense Cap = (55 / 45) × 23,500  
                    = 1.222... × 23,500  
                    = 28,722 (rounded)

Each Trooper provides 4 offense, so:

Troopers Allowed = 28,722 / 4  
                 = 7,180
                 


## 🕒 Cap Loosening Over Time

To encourage offense as the game progresses, the Anti-Turtle Cap System **loosens** after a certain point in time.

### ⏳ When Does It Loosen?

- **Start of loosening**: Day 3 (Tick 144)
- **Fully loosened**: Day 13 (Tick 144 + 10 × 48)

Between these ticks, the cap gradually loosens. Before tick 144, it’s fully tight. After tick 624, it’s at its most relaxed.

  

### 📉 How It Works

The system uses a **tightness factor** that starts at **1.0** (full cap pressure) and decreases to **0.5** (50% looser).  
This factor adjusts your offensive cap upward over time.

#### 🔍 Formula Overview:

```sql
IF CurrentTick < 3 * 48:
    CapTightness = 1.0

ELSE IF CurrentTick > (13 * 48):
    CapTightness = 0.5

ELSE:
    CapTightness = 1 - ((CurrentTick - 3*48) / (10*48)) * 0.5
```

Your final **offensive cap** is calculated like this:

```
OffensiveCap = (DefenseCap / 0.45) × 0.55
OffensiveCap = OffensiveCap / CapTightness
```

So as the cap loosens (CapTightness ↓), your offensive potential increases!  
At max looseness you can train offensive in a 2.44:1 ratio

