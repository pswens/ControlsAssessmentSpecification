# 9.3: Maintain and Enforce Network-Based URL Filters

Enforce and update network-based URL filters to limit an enterprise
asset from connecting to potentially malicious or unapproved websites.
Example implementations include category-based filtering,
reputation-based filtering, or through the use of block lists. Enforce
filters for all enterprise assets.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration
    Processs

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standards
3.  `GV5`: Authorized software inventory

## Operations

1.  Use `GV1` to identify and enumerate enterprise assets capable of
    supporting network-based URL filters (M1)

2.  Use `GV5` to identify authorized web browsers/clients

3.  

    For each asset identified in Operation 1 check to see if it is configured properly `GV3` to support authorized web browsers/clients from Operation 2

    :   1.  Identify and enumerate assets properly configured (M2)
        2.  Identify and enumerate assets not properly configured (M3)

## Measures

-   M1 = Count of enterprise assets capable of supporting network-based
    URL filters
-   M2 = Count of assets properly configured to support network-based
    URL filters
-   M3 = Count of assets not properly configured to support
    network-based URL filters

## Metrics

Coverage \^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of assets configured to use authorized network-based URL filters
    * - **Calculation**
      - :code:`M2 / M1`
