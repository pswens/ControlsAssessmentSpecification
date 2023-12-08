# 8.7: Collect URL Request Audit Logs

Collect URL request audit logs on enterprise assets, where appropriate
and supported.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Detect              2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standards

## Operations

1.  Use `GV1` to identify and enumerate assets that support URL logging
    (M1)

2.  

    For each asset identified in Operation 1, use `GV3` to check configurations for URL logging

    :   1.  Identify and enumerate assets properly configured for
            logging (M2)
        2.  Identify and enumerate assets not properly configured for
            logging (M3)

## Measures

-   M1 = Count of assets capable of supporting URL logging
-   M2 = Count of assets properly configured for URL logging
-   M3 = Count of assets not properly configured for URL logging

## Metrics

### Configuration Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of assets properly cofigured for |
|                 | | URL logging                                     |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / M1`                                         |
+-----------------+---------------------------------------------------+
