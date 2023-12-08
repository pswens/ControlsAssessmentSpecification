3.10: Encrypt Sensitive Data in Transit
================================== Encrypt sensitive data in transit.
Example implementations can include, Transport Layer Security (TLS) and
Open Secure Shell (OpenSSH).

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Protect             2, 3

# Dependencies

-   Safeguard 3.2: Establish and Maintain a Data Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

# Inputs

1.  `GV12`: Sensitive data Inventory
2.  `GV5`: Configuration Information

# Operations

1.  For each item in `GV12`, identify the means and components for
    encrypting data in transit.

2.  

    Compare the output of Operation 1 with `GV5` to check appropriate approved configurations

    :   1.  Enumerate the data items in `GV12` that are properly
            configured (M2)
        2.  Enumerate the data items in `GV12` that are improperly
            configured (M3)

# Measures

-   M1 = Count of items in `GV12`
-   M2 = Count of data with properly configured encryption components
-   M3 = Count of data with improperly configured encryption components

# Metrics

## Coverage

+-----------------+-------------------------------------+------------+
| **Metric**      | | The percentage of sensitive data  | | transit. |
|                 |   properly configured to be         |            |
|                 |   encrypted in                      |            |
+-----------------+-------------------------------------+------------+
| **Calculation** | `M2 / M1`                           |            |
+-----------------+-------------------------------------+------------+
