---
title: Mine Gold
description: 
published: true
date: 2025-04-19T16:45:56.404Z
tags: 
editor: markdown
dateCreated: 2025-04-19T16:45:56.404Z
---

## 📢 Update: Changes to the Gold Mining Formula!

Hello everyone!

We've recently updated the gold mining mechanics to place greater emphasis on early-game growth while introducing deeper strategic decision-making in mid and late-game phases. The new balance means that investing in probes will yield higher returns initially but becomes strategically nuanced later, especially when considering investments in Star Mines.

Here's an overview of what's changing:

### 🛠️ **Old Formula**
Previously, the gold mined was calculated simply:
- Up to 15,000 probes:
  ```
  gold = probes × 6.5
  ```
- Beyond 15,000 probes:
  ```
  gold = (15,000 × 6.5) + ((probes - 15,000) × 2.5)
  ```

This provided a steady but linear progression.

### ✨ **New Formula**
The updated formula introduces a dynamic calculation to encourage more strategic gameplay:

- **0 to 15,000 probes:** 
  ```
  gold = 6.5 × probes
  ```

- **15,001 to 30,000 probes:**
  ```
  gold = -9,809,020 × (probes ^ -0.378512) + 355,088
  ```

- **30,001 to 859,400 probes:**
  ```
  gold = 14.1692 × (probes ^ 0.847744) + 68,473.3
  ```

- **859,401 probes and above:**
  ```
  gold = 1.5 × probes + 300,000
  ```

### 📊 **Comparisons by Game Phase**

**Early Game Comparison**

![gold_mined_comparison_probes_10000_to_100000.png](/gold_mined_comparison_probes_10000_to_100000.png)
![gold_per_probe_comparison_probes_10000_to_100000.png](/gold_per_probe_comparison_probes_10000_to_100000.png)

| Probes | Old Gold | New Gold | Old Gold/Probe | New Gold/Probe |
|--------|----------|----------|----------------|----------------|
| 10,000 | 65,000   | 65,000   | 6.5            | 6.5            |
| 20,000 | 110,000  | 124,076  | 5.5            | 6.2038         |
| 30,000 | 135,000  | 156,943  | 4.5            | 5.2314         |
| 40,000 | 160,000  | 181,378  | 4.0            | 4.5344         |
| 50,000 | 185,000  | 204,890  | 3.7            | 4.0978         |
| 60,000 | 210,000  | 227,692  | 3.5            | 3.7949         |
| 70,000 | 235,000  | 249,919  | 3.3571         | 3.5703         |
| 80,000 | 260,000  | 271,667  | 3.25           | 3.3958         |
| 90,000 | 285,000  | 293,003  | 3.1667         | 3.2556         |
|100,000 | 310,000  | 313,981  | 3.1            | 3.1398         |

**Mid-Game Comparison**
![gold_mined_comparison_probes_100000_to_500000.png](/gold_mined_comparison_probes_100000_to_500000.png)
![gold_per_probe_comparison_probes_100000_to_500000.png](/gold_per_probe_comparison_probes_100000_to_500000.png)

| Probes | Old Gold | New Gold | Old Gold/Probe | New Gold/Probe |
|--------|----------|----------|----------------|----------------|
|100,000 | 310,000  | 313,981  | 3.1            | 3.1398         |
|150,000 | 435,000  | 414,688  | 2.9            | 2.7646         |
|200,000 | 560,000  | 510,309  | 2.8            | 2.5515         |
|250,000 | 685,000  | 602,320  | 2.74           | 2.4093         |
|300,000 | 810,000  | 691,550  | 2.7            | 2.3052         |
|350,000 | 935,000  | 778,534  | 2.6714         | 2.2244         |
|400,000 |1,060,000 | 863,639  | 2.65           | 2.1591         |
|450,000 |1,185,000 | 947,136  | 2.6333         | 2.1047         |
|500,000 |1,310,000 |1,029,228 | 2.62           | 2.0585         |

**Late Game Comparison**

![gold_mined_comparison_probes_500000_to_1000000.png](/gold_mined_comparison_probes_500000_to_1000000.png)
![gold_per_probe_comparison_probes_500000_to_1000000.png](/gold_per_probe_comparison_probes_500000_to_1000000.png)

| Probes | Old Gold | New Gold | Old Gold/Probe | New Gold/Probe |
|--------|----------|----------|----------------|----------------|
|500,000 |1,310,000 |1,029,228 | 2.62           | 2.0585         |
|600,000 |1,560,000 |1,189,816 | 2.6            | 1.983          |
|700,000 |1,810,000 |1,346,359 | 2.5857         | 1.9234         |
|800,000 |2,060,000 |1,499,522 | 2.575          | 1.8744         |
|900,000 |2,310,000 |1,650,000 | 2.5667         | 1.8333         |
|1,000,000|2,560,000|1,800,000 | 2.56           | 1.8            |

### 📈 **Why the Change?**
The goal is to encourage strategic decision-making regarding probe investments and balance the interaction between probes and Star Mines. Early-game probes now deliver stronger returns, promoting initial growth. However, in later stages, strategic consideration becomes crucial, as the diminishing returns per probe mean players will need to balance probe investments with other growth opportunities such as Star Mines.
