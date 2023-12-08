# 6.3: Require MFA for Externally-Exposed Applications

Require all externally-exposed enterprise or third-party applications to
enforce MFA, where supported. Enforcing MFA through a directory service
or SSO provider is a satisfactory implementation of this Safeguard.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             1, 2, 3

## Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process
-   Safeguard 5.1: Establish and Maintain an Inventory of Accounts

## Inputs

1.  `GV5`: Authorized Software Inventory
2.  `GV22`: Inventory of Accounts
3.  `GV3`: Configuration Standard

## Operations

1.  Use Input 1 to identify and enumerate externally exposed and third
    party applications

2.  Using the output of Operation 1 and `GV22` identify and enumerate
    all user accounts associated with the applications (M1)

3.  

    For each account identified in Operation 2 use `GV3` to

    :   1.  Identify and enumerate accounts properly configured to
            require MFA (M2)
        2.  Identify and enumerate accounts not properly configured to
            require MFA (M3)

## Measures

-   M1 = Count of accounts associated with externally exposed and third
    party applications
-   M2 = Count of accounts properly configured to require MFA
-   M3 = Count of accounts not properly configured to require MFA

## Metrics

### Coverage

+-----------------+------------------------+------------------------+
| **Metric**      | | The percentage of    | | properly configured  |
|                 |   externally exposed   |   for MFA              |
|                 |   and third party      |                        |
|                 |   application accounts |                        |
+-----------------+------------------------+------------------------+
| **Calculation** | `M2 / M1`              |                        |
+-----------------+------------------------+------------------------+
