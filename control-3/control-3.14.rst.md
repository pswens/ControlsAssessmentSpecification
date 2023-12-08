# 3.14: Log Sensitive Data Access

Log sensitive data access, including modification and disposal.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Detect              3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV5`: Authorized software inventory
2.  `GV19`: Enterprise assets storing sensitive data
3.  `GV3`: Configuration Standards

## Operations

1.  Using `GV3` identify authorized logging software

2.  

    For each asset in `GV19`, use the output from Operation 1

    :   1.  Identify and enumerate assets with logging software
            installed (M2)
        2.  Identify and enumerate assets that do not have logging
            software installed (M3)

3.  

    For logging software installed check configuration using `GV3`

    :   1.  Identify and enumerate software that is properly configured
            (M4)
        2.  Identify and enumerate software that is improperly
            configured (M5)

## Measures

-   M1 = Count of `GV19`
-   M2 = Count of assets storing sensitive data with logging software
-   M3 = Count of assets storing sensitive data without logging software
-   M4 = Count of assets with properly configured logging
-   M5 = Count of assets with imporperly configured logging

## Metrics

### Coverage

+-----------------+------------------------------+-------------------+
| **Metric**      | | The percentage of properly | | sensitive data. |
|                 |   configured logging on      |                   |
|                 |   assets storing             |                   |
+-----------------+------------------------------+-------------------+
| **Calculation** | `M4 / M1`                    |                   |
+-----------------+------------------------------+-------------------+
