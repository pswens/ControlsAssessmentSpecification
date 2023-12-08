4.11: Enforce Remote Wipe Capability on Portable End-User Devices
=============================================================== Remotely
wipe enterprise data from enterprise-owned portable end-user devices
when deemed appropriate such as lost or stolen devices, or when an
individual no longer supports the enterprise.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Devices      Protect             2, 3

# Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safegaurd 4.1: Establish and Maintain a Secure Configuration Process

# Inputs

1.  :code:\`GV21: Portable end-user devices
2.  `GV3`: Configuration standards

# Operations

1.  Use `GV21` to identify and enumerate portable end-user devices that
    support remote wipe (M1)

2.  

    Use `GV3` to check configuration for remote wipe on portable devices capable of supporting as identified in Operation 1

    :   1.  Identify and enumerate portable devices with properly
            configured remote wipe (M2)
        2.  Identify and enumerate portable devices with improperly
            configured remote wipe (M3)

# Measures

-   M1 = Count of portable devices capable of supporting remote wipe
-   M2 = Count of properly configured portable devices
-   M3 = Count of improperly configured portable devices

# Metrics

## Compliance of Remote Wipe

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of portable devices with         |
|                 |   properly configured                             |
|                 | | remote wipe.                                    |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / M1`                                         |
+-----------------+---------------------------------------------------+
