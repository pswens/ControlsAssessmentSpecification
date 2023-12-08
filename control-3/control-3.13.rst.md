3.13: Deploy a Data Loss Prevention Solution
================================== Implement an automated tool, such as
a host-based Data Loss Prevention (DLP) tool to identify all sensitive
data stored, processed, or transmitted through enterprise assets,
including those located onsite or at a remote service provider, and
update the enterprise\'s sensitive data inventory.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Protect             3

# Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 3.2: Establish and Maintain a Data Inventory

# Inputs

1.  `GV18`: Enterprise assets storing, processing, or transmitting
    sensitive data
2.  `GV5`: Authorized Software inventory
3.  `GV3`: Configuration Standards

# Operations

1.  Use `GV5` to identify and enumerate all data loss prevention
    software

2.  

    Compare `GV18` and the output of Operation 1

    :   1.  Identify and enumerate each asset in `GV18` with data loss
            prevention software installed (M2)
        2.  Identify and enumerate each asset in `GV18` without data
            loss prevention software installed (M3)

3.  

    For assets with data loss prevention installed from Operation 2.1 check `GV3` for configuration information

    :   1.  Identify and enumerate assets with properly configured data
            lass prevention software (M4)
        2.  Identify and enumerate assets with improperly configured
            data lass prevention software (M5)

# Measures

-   M1 = Count of `GV18`
-   M2 = Count of assets with data loss prevention software
-   M3 = Count of assets without data loss prevention software
-   M4 = Count of assets with properly configured data loss prevention
    software
-   M5 = Count of assets with improperly configured data loss prevention
    software

# Metrics

## Coverage

+-----------------+------------------------+------------------------+
| **Metric**      | | The percentage of    | | data loss prevention |
|                 |   assets covered by at |   software instance.   |
|                 |   least one properly   |                        |
|                 |   configured           |                        |
+-----------------+------------------------+------------------------+
| **Calculation** | `M4 / M1`              |                        |
+-----------------+------------------------+------------------------+
