# 8.12: Collect Service Provider Logs

Collect service provider logs, where supported. Example implementations
include collecting authentication and authorization events, data
creation and disposal events, and user management events

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Detect              3

## Dependencies

-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process
-   Safeguard 15.1: Establish and Maintain an Inventory of Service
    Providers

## Inputs

1.  `GV29`: Inventory of service providers
2.  `GV3`: Configuration standard

## Operations

1.  For each service provided in `GV29` identify and enumerate service
    providers that supports logging (M1)

2.  

    Use service provider identified in Operation 1, use `GV3` to check configurations

    :   1.  Identify and enumerate service providers properly configured
            to collect logs (M2)
        2.  Identify and enumerate service providers not properly
            configured to collect logs (M3)

## Measures

-   M1 = Count of service providers that support logging
-   M2 = Count of service providers configured to collect logs
-   M3 = Count of service providers not configured to collect logs

## Metrics

### Coverage

+-----------------+----------------------------------------------------------+
| **Metric**      | | The percentage of service providrs proverly configured |
|                 | | to collect logs                                        |
+-----------------+----------------------------------------------------------+
| **Calculation** | `M2 / M1`                                                |
+-----------------+----------------------------------------------------------+
