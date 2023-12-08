# 13.1: Centralize Security Event Alerting

Centralize security event alerting across enterprise assets for log
correlation and analysis. Best practice implementation requires the use
of a SIEM, which includes vendor-defined event correlation alerts. A log
analytics platform configured with security-relevant correlation alerts
also satisfies this Safeguard.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Detect              2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory

## Inputs

1.  Location of `GV42`: log correlation or log analytic tool
2.  `GV1`: Enterprise asset inventory

## Operations

1.  

    Check if Input 1 exists within the enterprise

    :   1.  If Input 1 exists, M1 = 1
        2.  If Input 1 does not exist, M1 = 0

2.  Use `GV1` to identify and enumerate enterprise assets that produce
    security event logs (M2)

3.  

    For every asset identified in Operation 2, check if logs are centralized at the location of the log correlation or log analytic tool Input 1

    :   1.  Identify and enumerate assets whose logs are centralized
            (M3)
        2.  Identify and enumerate assets whose logs are not centralized
            (M4)

## Measures

-   M1 = Output of Operation 1
-   M2 = Count of assets that produce security event logs
-   M3 = Count of assets with security event logs being centralized
-   M4 = Count of assets with security event logs not being centralized

## Metrics

If M1 is 0, this Safeguard receives a failing score. The other metrics
don\'t apply.

### Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of asses whose security even     |
|                 |   logs are centralized                            |
+-----------------+---------------------------------------------------+
| **Calculation** | `M3 / M2`                                         |
+-----------------+---------------------------------------------------+
