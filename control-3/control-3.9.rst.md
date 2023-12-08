3.9: Encrypt Data on Removable Media ==================================
Encrypt data on removable media.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Protect             2, 3

# Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

# Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized software inventory
3.  `GV3`: Configuration Standards

Assumptions \-\-\-\-\-\-\-\-\--#. Enterprise asset inventory includes
removable media

# Operations

1.  Use `GV1` to identify and enumerate assets authorized to support
    removeable media (M1)

2.  

    Use `GV5` to identify encryption software installed on assets identified in Operation 1 (M1)

    :   1.  Enumerate the number of assets with encryption software
            installed (M2)
        2.  Enumerate the number of assets without encryption software
            installed (M3)

3.  

    For assets identified in Operation 2.1, use `GV3` to check configurations of encryption software

    :   1.  Enumerate assets that have properly configured encryption
            software (M4)
        2.  Enumerate assets that have improperly configured encryption
            software(M5)

# Measures

-   M1 = Count of assets authorized to support removeable media
-   M2 = Count of authorized assets with encryption software installed
-   M3 = Count of authorized assets without encryption software
    installed
-   M4 = Count of authorized assets with properly configured encryption
    software
-   M5 = Count of authorized assets with improperly configured
    encryption software

# Metrics

## Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of appropriately configured      |
|                 |   assets to support removeable media.             |
+-----------------+---------------------------------------------------+
| **Calculation** | `M4 / M1`                                         |
+-----------------+---------------------------------------------------+
