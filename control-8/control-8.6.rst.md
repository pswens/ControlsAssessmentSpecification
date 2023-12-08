# 8.6: Collect DNS Query Audit Logs

Collect DNS query audit logs on enterprise assets, where appropriate and
supported.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Detect              2, 3

## Dependencies

-   Safegaurd 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standards

Assumptions \-\-\-\-\-\-\-\-\--#. The enterprise maintains their own
internal DNS Servers.

## Operations

1.  Use Input 1 `GV1` to identify and enumerate internal DNS Servers
    (M1)

2.  

    Check the configurations `GV3` of each DNS Server identified in Operation 1

    :   1.  Identify and enumerate DNS servers properly configured to
            collect logs (M2)
        2.  Identify and enumerate DNS servers not properly configured
            to collect logs (M3)

## Measures

-   M1 = Count of internal DNS servers
-   M2 = Count of properly configured DNS servers
-   M3 = Count of DNS servers not properly configured DNS servers

## Metrics

DNS Configuration Coverage \^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of properly configured DNS servers to meet
        | logging requirements.
    * - **Calculation**
      - :code:`M2 / M1`
