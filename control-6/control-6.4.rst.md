# 6.4: Require MFA for Remote Network Access

Require MFA for remote network access.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             1, 2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standards

## Operations

1.  Using `GV1` as a guide, identify and enumerate all authorized remote
    assets (M1)

2.  

    For each asset identified in Operation 1, check configurations `GV3`

    :   1.  Identify and enumerate assets properly configured to require
            MFA (M2)
        2.  Identify and enumerate assets not properly configured to
            require MFA (M3)

## Measures

-   M1 = Count of remote assets
-   M2 = Count of remote assets properly configured to require MFA
-   M3 = Count of remote assets not properly configured to require MFA

## Metrics

### Coverage

+------------+-------------------------------------------+-----------+
| **Metric** | | The percentage of remote assets poperly | `M2 / M1` |
|            |   configured to require MFA               |           |
+------------+-------------------------------------------+-----------+
