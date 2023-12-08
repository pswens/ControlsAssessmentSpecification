# 8.2: Collect Audit Logs

Collect audit logs. Ensure that logging, per the enterprise's audit log
management process, has been enabled across enterprise assets.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Detect              1, 2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process
-   Safeguard 8.1: Establish and Maintain an Audit Log Management
    Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standards
3.  `GV26`: Enterprise\'s audit log management process

## Operations

1.  Use `GV1` to identify and enumerate assets capable of supporting
    logging `GV27` (M1)

2.  

    Use `GV26` and `GV3` as guides to determine, for each asset identifed in Operation 1 is configured to log events as outlined by the enterprise\'s process

    :   1.  Identify and enumerate assets properly configured to log
            events per the process (M2)
        2.  Identify and enumerate assets not properly configured to log
            events per the process (M3)

## Measures

-   M1 = Count of assets capable of supporting logging
-   M2 = Count of properly configured assets to log events per the audit
    log management process
-   M3 = Count of assets not properly configured to log events per the
    audit log management process

## Metrics

### Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The ratio of logging capable assets properly    |
|                 |   configured per the                              |
|                 | | audit log management process.                   |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / M1`                                         |
+-----------------+---------------------------------------------------+
