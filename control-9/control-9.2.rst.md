# 9.2: Use DNS Filtering Services

Use DNS filtering services on all enterprise assets to block access to
known malicious domains.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             1, 2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized software inventory
3.  `GV3`: Configuration standards

## Operations

1.  Use `GV1` to identify and enumerate assets that support DNS
    filtering (M1)

2.  Use `GV5` to identify and enumerate authorized DNS filtering
    services

3.  

    For each asset identified in Operation 1 check to see if it is configured properly `GV3` to support authorized DNS filtering services from Operation 2

    :   1.  Identify and enumerate assets properly configured (M2)
        2.  Identify and enumerate assets not properly configured (M3)

## Measures

-   M1 = Count of enterprise assets capable of supporting DNS filtering
-   M2 = Count of assets properly configured to support DNS filtering
-   M3 = Count of assets not properly configured to support DNS
    filtering

## Metrics

DNS Filtering Coverage \^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of assets configured to use authorized DNS filtering services
    * - **Calculation**
      - :code:`M2 / M1`
