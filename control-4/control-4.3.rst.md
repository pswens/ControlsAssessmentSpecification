4.3: Configure Automatic Session Locking on Enterprise Assets
========================================================= Configure
automatic session locking on enterprise assets after a defined period of
inactivity. For general purpose operating systems, the period must not
exceed 15 minutes. For mobile end-user devices, the period must not
exceed 2 minutes.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             1, 2, 3

# Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

# Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized software Inventory
3.  `GV3`: Configuration standard

# Operations

1.  Identify and enumerate assets within `GV1` that support automatic
    locking due to inactivity (M1)

2.  Use `GV5` to identify and enumerate assets from Operation 1 with
    authorized software installed (M2)

3.  

    Check the configurations for the software using `GV3`

    :   1.  For general computing assets, enumerate those assets with
            properly configured automatic locking (15 minutes or less)
            (M3)
        2.  For general computing assets, enumerate those assets with
            improperly configured automatic locking (greater than 15
            minutes) (M4)
        3.  For mobile assets, enumerate those assets with properly
            configured automatic locking (2 minutes or less) (M5)
        4.  For mobile assets, enumerate those assets with improperly
            configured automatic locking (greater than 2 minutes) (M6)

# Measures

-   M1 = Count of assets capable of supporting automatic lockout
-   M2 = Count of assets with authorized software installed to allow
    lockout
-   M3 = Count of general computing assets with properly configured
    lockout
-   M4 = Count of general computing assets with improperly configured
    lockout
-   M5 = Count of mobile assets with properly configured lockout
-   M6 = Count of mobile assets with improperly configured lockout

# Metrics

## Properly Configured Assets

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of assets properly configured    |
|                 |   for automatic lockout.                          |
+-----------------+---------------------------------------------------+
| **Calculation** | `(M3 + M5) / M1`                                  |
+-----------------+---------------------------------------------------+
