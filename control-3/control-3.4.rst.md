# 3.4: Enforce Data Retention

Retain data according to the enterprise's data management process. Data
retention must include both minimum and maximum timelines.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Protect             1, 2, 3

## Dependencies

-   Safeguard 3.1: Establish and Maintain a Data Management Process
-   Safeguard 3.2: Establish and Maintain a Data Inventory

## Inputs

1.  `GV15`: Data Retention Limits outlined in the data management
    process
2.  `GV11`: Portion of data management process addressing data
    sensitivity
3.  `GV12`: Sensitive Data Inventory

## Operations

1.  

    For each sensitive data type covered in `GV11`

    :   1.  Enumerate the number of types of sensitivity (`GV17`: M1),
            at a minimum one to deferrentiate sensitive data from other
            data
        2.  Identify and enumerate if each type has a minimum retention
            time (M2) as defined by `GV15`
        3.  Identify and enumerate if each type has a maximum retention
            time (M3) as defined by :code:\`GV15

2.  

    Using the output of Operation 1.1 and 1.2, check the data inventory `GV12` for enforcement of data retention

    :   1.  Identify and enumerate items in the inventory that comply
            with retention timelines (M4)
        2.  Identify and enumerate items in the inventory that do not
            comply with retention timelines (M5)

## Measures

-   M1 = Count of sensitivity types that require retention timelines
-   M2 = Count of sensitivity types that ainclude minimum retention
    times
-   M3 = Count of sensitivity types that ainclude maximum retention
    times
-   M4 = Count of data in inventory that comply with retention policy
-   M5 = Count of data in inventory that do not comply with retention
    policy
-   M6 = Count of `GV12`

## Metrics

If `GV15` is 0, this safeguard receives a failing score. The other
metrics don\'t apply.

### Completeness of Policy

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of sensitivity types that        |
|                 |   include minimum retention timelines             |
+-----------------+---------------------------------------------------+
| **Calculation** | | :code: [M2 / M1]{.title-ref}                    |
+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of sensitivity types that        |
|                 |   include maximum retention timelines             |
+-----------------+---------------------------------------------------+
| **Calculation** | | :code: [M3 / M1]{.title-ref}                    |
+-----------------+---------------------------------------------------+

### Enforcement of Retention Policy

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of sensitivity data that         |
|                 |   complies with retention policy                  |
+-----------------+---------------------------------------------------+
| **Calculation** | | `M4 / M6`                                       |
+-----------------+---------------------------------------------------+
