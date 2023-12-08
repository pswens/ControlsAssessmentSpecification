# 11.3: Protect Recovery Data

Protect recovery data with equivalent controls to the original data.
Reference encryption or data separation, based on requirements.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Protect             1, 2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV33`: Assets that are in-scope for automated backups
2.  `GV34`: Assets with authorized backup software installed
3.  `GV3`: Configuration Standard

## Operations

1.  

    For each asset with backup software installed, use `GV3` to check if encryption is configured for backups

    :   1.  Identify and enumerate assets with software configured to
            encrypt backups (M2)
        2.  Identify and enumerate assets with software not configured
            to encrypt backups (M3)

## Measures

-   M1 = Count of Input 1: `GV33`
-   M2 = Count of software configured to encrypt backups
-   M3 = Count of software not configured to encrypt backups

## Metrics

### Coverage

+-----------------+------------------------+-----------------------+
| **Metric**      | | The percentage of    | | to encrypt backups. |
|                 |   in-scope assets with |                       |
|                 |   backup software      |                       |
|                 |   properly configured  |                       |
+-----------------+------------------------+-----------------------+
| **Calculation** | `M2 / M1`              |                       |
+-----------------+------------------------+-----------------------+
