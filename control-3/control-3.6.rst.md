# 3.6: Encrypt Data on End-User Devices

Encrypt data on end-user devices containing sensitive data. Example
implementations can include, Windows BitLocker®, Apple FileVault®,
Linux® dm-crypt.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Devices      Protect             1, 2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized software inventory
3.  `GV3`: Configuration Standards

## Operations

1.  

    For each asset in `GV1`, identify end-user devices

    :   1.  Enumerate the end-user devices (M1)
        2.  Use `GV5` to identify and enumerate the assets that have
            encryption software installed (M2)
        3.  Use `GV5` to identify and enumerate the assets without
            encryption software (M3)

2.  

    For each encryption software installed on assets (M2), use `GV3` to determine whether the software is properly configured

    :   1.  Enumerate the encryption software that is properly
            configured (M4)
        2.  Enumerate the encryption software that is improperly
            configured (M5)

## Measures

-   M1 = Count of approved end-user devices
-   M2 = Count of approved end-user devices with encryption software
    installed
-   M3 = Count of approved end-user devices without encryption software
-   M4 = Count of properly configured end-user devices
-   M5 = Count of improperly configured end-user devices

## Metrics

### Installed Software Coverage

+-----------------+------------------------------------+-------------+
| **Metric**      | | The percentage of approved       | | software. |
|                 |   mobile devices that are equipped |             |
|                 |   with approved encryption         |             |
+-----------------+------------------------------------+-------------+
| **Calculation** | `M2 / M1`                          |             |
+-----------------+------------------------------------+-------------+

Appropriately Configured Devices \^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of approved mobile devices equipped with approved encryption software
      - | that meet or exceed the approved configuration policy.
    * - **Calculation**
      - :code:`M3 / M1`
