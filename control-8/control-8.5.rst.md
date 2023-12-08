# 8.5: Collect Detailed Audit Logs

Configure detailed audit logging for enterprise assets containing
sensitive data. Include event source, date, username, timestamp, source
addresses, destination addresses, and other useful elements that could
assist in a forensic investigation.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Detect              2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory

## Inputs

1.  `GV18`: Enterprise assets storing, processing, and transmitting
    sensitive data
2.  `GV26`: Enterprise\'s audit log management process
3.  `GV3`: Configuration standards

## Operations

1.  

    Review `GV26` for detailed logging requirements such as event source, date, username, timestamp, source addresses, and destination addresses.

    :   1.  For each detailed logging requirement included, assign a
            value of 1. Sum all requirements included. (M2)

2.  

    For each asset in `GV18` check configuraions using `GV3` as a guide

    :   1.  Identify and enumerate assets properly configured to collect
            detailed logging requirements (M3)
        2.  Identify and enumerate assets not properly configured to
            collect detailed logging requirements (M4)

## Measures

-   M1 = Count of assets capable of supporting logging `GV27`
-   M2 = Count of detailed logging requirements included in log
    management process
-   M3 = Count of assets properly configured to collect detailed logs
-   M4 = Count of assets not properly configured to collect detailed
    logs

## Metrics

Completeness of Process \^\^\^\^\^\^\^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of detailed logging requirements included in the 
      - | logging manangement process.
    * - **Calculation**
      - :code:`M2 / 6`

Logging Coverage \^\^\^\^\^\^\^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of assets properly configured to collect 
      - | detailed logs.
    * - **Calculation**
      - :code:`M3 / M1`
