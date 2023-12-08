# 5.6: Centralize Account Management

Centralize account management through a directory or identity service.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory

## Inputs

1.  `GV1`: Enterprise asset inventory

## Operations

1.  Using `GV1` identify and enumerate centralized auhtentication points
    (M1)

2.  

    For each centralized authentication point indentifed in Operation 1, determine whether it is necessary or can be consolidated

    :   1.  Identify and enumerate authentication points that are
            unnecesary or can be consolidated (M2)
        2.  Identify and enumerate authentication points that are
            necesary and cannot be consolidated (M3)

## Measures

-   M1 = Count of cetralized authentication points in the enterprise
-   M2 = Count of unnecessary centralized authentication points
-   M3 = Count of necessary centralized authentication points

## Metrics

### Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | Percentage of properly centralized              |
|                 |   aunthentication points                          |
+-----------------+---------------------------------------------------+
| **Calculation** | `M3 / M1`                                         |
+-----------------+---------------------------------------------------+
