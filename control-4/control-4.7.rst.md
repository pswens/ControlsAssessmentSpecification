4.7: Manage Default Accounts on Enterprise Assets and Software
========================================================= Manage default
accounts on enterprise assets and software, such as root, administrator,
and other pre-configured vendor accounts. Example implementations can
include: disabling default accounts or making them unusable.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             1, 2, 3

# Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 5.2: Use Unique Passwords

# Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized software inventory
3.  `GV20`: Unique password policy

# Operations

1.  Use `GV5` to identify and enumerate authorized operating software,
    applications, and third-party software that contain default accounts
    (M1)

2.  Use `GV1` to identify and enumerate assets with software, from
    Operation 1, installed (M2)

3.  For each identified in Operation 2, enumerate default accounts (M3)

4.  

    Check if default accounts can be disabled

    :   1.  Enumerate accounts that are disabled (M4)
        2.  Enumerate accounts that are enabled (M5)

5.  

    If account cannot be disabled, ensure to change default passwords according to the `GV20`: enterprise\'s unique password policy

    :   1.  Enumerate accounts with changed passwords (M6)

# Measures

-   M1 = Count of software that uses default accounts
-   M2 = Count of assets with software installed that uses default
    accounts
-   M3 = Count of default accounts identified
-   M4 = Count of default accounts that have been disabled
-   M5 = Count of default accounts that are enabled
-   M6 = Count of enabled default accounts with changed passwords

# Metrics

Unusable Default Accounts \^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of default accounts that have been rendered unusable
    * - **Calculation**
      - :code:`(M4 + M6) / M3`
