# 10.3: Disable Autorun and Autoplay for Removable Media

Disable autorun and autoplay auto-execute functionality for removable
media.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Devices      Protect             1, 2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standards

## Operations

1.  Use `GV1` to identify and enumerate enterprise assets capable of
    performing autorun, autoplay, and auto-execute functions (M1)

2.  

    Check the configurations `GV3` of each asset identified in Operation 1 to see if the autorun, autoplay, and auto-execute functions are disabled

    :   1.  Identify and enumerate properly configured assets (M2)
        2.  Identify and enumerate improperly configured assets (M3)

## Measures

-   M1 = Count of assets capable of performing autorun, autoplay, and
    auto-excecute functions
-   M2 = Count of assets properly configured to disable functions
-   M3 = Count of assets not properly configured to disable functions

## Metrics

### Compliance

+-----------------+------------------------+------------------------+
| **Metric**      | | The percentage of    | | and autoexecute      |
|                 |   assets properly      |   functions.           |
|                 |   configured to        |                        |
|                 |   disable autorun,     |                        |
|                 |   autoplay             |                        |
+-----------------+------------------------+------------------------+
| **Calculation** | `M2 / M1`              |                        |
+-----------------+------------------------+------------------------+
