# 11.4: Establish and Maintain an Isolated Instance of Recovery Data 

Establish and maintain an isolated instance of recovery data. Example
implementations include, version controlling backup destinations through
offline, cloud, or off-site systems or services.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Recover             1, 2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV33`: Assets that are in-scope for automated backups
2.  `GV34`: Assets with authorized backup software installed
3.  `GV3`: Configuration standards

Assumptions \-\-\-\-\-\-\-\-\--#. Configuration for backups will contain
information about destination of backups

## Operations

1.  

    For each asset in Input 2 `GV34`, use configuration standards in `GV3` to check destination of backups

    :   1.  Identify and enumerate assets properly configured to send
            backups to an isolated instance (M2)
        2.  Identify and enumerate assets not properly configured to
            send backups to an isolated instance (M3)

## Measures

-   M1 = Count of Input 1 `GV33`
-   M2 = Count of assets with backups sent to an isolated instance
-   M3 = Count of assets with backups not sent to an isolated instance

## Metrics

### Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of assets configured to send     |
|                 |   backups to an isolated instance                 |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / M1`                                         |
+-----------------+---------------------------------------------------+
