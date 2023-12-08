# 6.7: Centralize Access Control

Centralize access control for all enterprise assets through a directory
service or SSO provider, where supported.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized software inventory

## Operations

1.  Use `GV5` to identify all directory and SSO services

2.  Use `GV1` to identify and enumerate assets that support directory
    and SSO services (M1)

3.  

    Check the output of Operations 1 and 2 to ensure each asset is covered by at least one directory or SSO service

    :   1.  Identify and enumerate assets that are covered by at least
            one directory or SSO services (M2)
        2.  Identify and enumerate assets that are not covered by at
            least one directory or SSO service (M3)

## Measures

-   M1 = Count of assets capable of supporing directory and/or SSO
    services
-   M2 = Count of assets covered by at least one directory or SSO
    service
-   M3 = Count of assets not covered by at least one directory or SSO
    service

## Metrics

### Coverage

+-----------------+------------------------+------------------------+
| **Metric**      | | The percentage of    | | covered by at least  |
|                 |   assets that can      |   one directory or SSO |
|                 |   support directory    |   service.             |
|                 |   and SSO service      |                        |
+-----------------+------------------------+------------------------+
| **Calculation** | `M2 / M1`              |                        |
+-----------------+------------------------+------------------------+
