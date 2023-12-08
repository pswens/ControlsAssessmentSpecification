# 8.9: Centralize Audit Logs

Centralize, to the extent possible, audit log collection and retention
across enterprise assets.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Detect              2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory

## Inputs

1.  `GV27`: Assets capable of supporting logging
2.  `GV5`: Authorized software inventory

## Operations

1.  Use the software inventory `GV5` to identify and enumerate log
    aggregating software `GV28`

2.  

    For each asset capable of supporting logging, check if asset is covered by at least one log aggregating software

    :   1.  Identify and enumerate assets covered by at least one
            aggregating software (M2)
        2.  Identify and enumerate assets not covered by at least one
            aggregating software (M3)

## Measures

-   M1 = Count of `GV27`
-   M2 = Count of assets covered by at least one aggregating software
-   M3 = Count of assets not covered by at least one aggregating
    software

## Metrics

Log Aggregating \^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of log producing assets covered by aggregating
        | software.
    * - **Calculation**
      - :code:`M2 / M1`
