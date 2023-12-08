# 6.5: Require MFA for Administrative Access

Require MFA for all administrative access accounts, where supported, on
all enterprise assets, whether managed on-site or through a third-party
provider.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             1, 2, 3

## Dependencies

-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process
-   Safeguard 5.1: Establish and Maintain an Inventory of Accounts

## Inputs

1.  `GV22`: Inventory of accounts
2.  `GV3`: Configuration Standard

## Operations

1.  Using `GV22` identify and enumerate all administrative accounts (M1)

2.  

    For each administrative account identified in Operation 1 check configurations in `GV3`

    :   1.  Identify and enumerate administrative accounts properly
            configured to require MFA (M2)
        2.  Identify and enumerate administrative accounts not properly
            configure to require MFA (M3)

## Measures

-   M1 = Count of administrative accounts
-   M2 = Count of administrative accounts properly configured to require
    MFA
-   M3 = Count of administrative accounts not properly configured to
    require MFA

## Metrics

### Coverage

+-----------------+---------------------------------+----------------+
| **Metric**      | | The percentage of             | | require MFA. |
|                 |   administrative accounts       |                |
|                 |   properly configured to        |                |
+-----------------+---------------------------------+----------------+
| **Calculation** | `M2 / M1`                       |                |
+-----------------+---------------------------------+----------------+
