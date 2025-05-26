---
title: Bots Military Composition
description: 
published: true
date: 2025-05-26T15:53:01.762Z
tags: 
editor: markdown
dateCreated: 2025-05-26T15:46:51.588Z
---

# Bots Military Composition

Composition For round June 2025
```sql
    IF @AIAggressiness >= 10
    BEGIN
        SET @OffenseUnitMaintainPct = 0.5
        SET @BalanceUnitMaintainPct = 0.1
        SET @DefenseUnitMaintainPct = 0.4
    END ELSE IF @AIAggressiness = 9
    BEGIN
        SET @OffenseUnitMaintainPct = 0.4
        SET @BalanceUnitMaintainPct = 0.2
        SET @DefenseUnitMaintainPct = 0.4
    END ELSE  IF @AIAggressiness = 8
    BEGIN
        SET @OffenseUnitMaintainPct = 0.3
        SET @BalanceUnitMaintainPct = 0.3
        SET @DefenseUnitMaintainPct = 0.4
    END ELSE IF @AIAggressiness = 7
    BEGIN
        -- this guy is more turtly but 
        -- set at high aggeressiveness so he sends his tanks
        SET @OffenseUnitMaintainPct = 0.1
        SET @BalanceUnitMaintainPct = 0.4
        SET @DefenseUnitMaintainPct = 0.5
    END ELSE IF @AIAggressiness = 6 
    BEGIN
        SET @OffenseUnitMaintainPct = 0.4
        SET @BalanceUnitMaintainPct = 0.1
        SET @DefenseUnitMaintainPct = 0.5
    END ELSE IF @AIAggressiness = 5
    BEGIN
        SET @OffenseUnitMaintainPct = 0.3
        SET @BalanceUnitMaintainPct = 0.2
        SET @DefenseUnitMaintainPct = 0.5
    END ELSE IF @AIAggressiness = 4
    BEGIN
        SET @OffenseUnitMaintainPct = 0.2
        SET @BalanceUnitMaintainPct = 0.3
        SET @DefenseUnitMaintainPct = 0.5
    END ELSE IF @AIAggressiness = 3
    BEGIN
        SET @OffenseUnitMaintainPct = 0.4
        SET @BalanceUnitMaintainPct = 0.0
        SET @DefenseUnitMaintainPct = 0.6
    END ELSE IF @AIAggressiness = 2
    BEGIN
        SET @OffenseUnitMaintainPct = 0.3
        SET @BalanceUnitMaintainPct = 0.1
        SET @DefenseUnitMaintainPct = 0.6
    END ELSE IF @AIAggressiness = 1
    BEGIN
        SET @OffenseUnitMaintainPct = 0.2
        SET @BalanceUnitMaintainPct = 0.2
        SET @DefenseUnitMaintainPct = 0.6
    END ELSE IF @AIAggressiness <= 0
    BEGIN
        SET @OffenseUnitMaintainPct = 0.2
        SET @BalanceUnitMaintainPct = 0.1
        SET @DefenseUnitMaintainPct = 0.7
    END
```

composition before June 2025
```sql
IF @AIAggressiness >= 8
BEGIN
    SET @OffenseUnitMaintainPct = 0.4
    SET @BalanceUnitMaintainPct = 0.1
    SET @DefenseUnitMaintainPct = 0.5
END ELSE IF @AIAggressiness = 7
BEGIN
    SET @OffenseUnitMaintainPct = 0.4
    SET @BalanceUnitMaintainPct = 0.0
    SET @DefenseUnitMaintainPct = 0.6
END ELSE IF @AIAggressiness = 6 
BEGIN
    SET @OffenseUnitMaintainPct = 0.3
    SET @BalanceUnitMaintainPct = 0.3
    SET @DefenseUnitMaintainPct = 0.4
END ELSE IF @AIAggressiness = 5
BEGIN
    SET @OffenseUnitMaintainPct = 0.3
    SET @BalanceUnitMaintainPct = 0.2
    SET @DefenseUnitMaintainPct = 0.5
END ELSE IF @AIAggressiness = 4
BEGIN
    SET @OffenseUnitMaintainPct = 0.3
    SET @BalanceUnitMaintainPct = 0.1
    SET @DefenseUnitMaintainPct = 0.6
END ELSE IF @AIAggressiness = 3
BEGIN
    SET @OffenseUnitMaintainPct = 0.2
    SET @BalanceUnitMaintainPct = 0.4
    SET @DefenseUnitMaintainPct = 0.4
END ELSE IF @AIAggressiness = 2
BEGIN
    SET @OffenseUnitMaintainPct = 0.2
    SET @BalanceUnitMaintainPct = 0.3
    SET @DefenseUnitMaintainPct = 0.5
END ELSE IF @AIAggressiness = 1
BEGIN
    SET @OffenseUnitMaintainPct = 0.2
    SET @BalanceUnitMaintainPct = 0.2
    SET @DefenseUnitMaintainPct = 0.6
END ELSE IF @AIAggressiness <= 0
BEGIN
    SET @OffenseUnitMaintainPct = 0.2
    SET @BalanceUnitMaintainPct = 0.1
    SET @DefenseUnitMaintainPct = 0.7
END
```