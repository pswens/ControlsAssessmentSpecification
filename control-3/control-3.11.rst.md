3.11: Encrypt Sensitive Data At Rest ==================================
Encrypt sensitive data at rest on servers, applications, and databases
containing sensitive data. Storage-layer encryption, also known as
server-side encryption, meets the minimum requirement of this Safeguard.
Additional encryption methods may include application-layer encryption,
also known as client-side encryption, where access to the data storage
device(s) does not permit access to the plain-text data. .. list-table::
:header-rows: 1

> -   -   Asset Type
>     -   Security Function
>     -   Implementation Groups
>
> -   -   Data
>     -   Protect
>     -   2, 3

# Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory

# Inputs

1.  `GV12`: Sensitive data inventory
2.  `GV4`: Enterprise Network Architecture Documentation
3.  `GV18`: Enterprise assets storing sensitive data

# Operations

1.  Use `GV5` to identify and enumerate all encryption tools requiring
    secondary authentication systems (M1)

2.  Use `GV12` and `GV1` to identify and enumerate all enterprise assets
    storing sensitive data (`GV19`: M2)

3.  

    Compare the output of Operation 1 and Operation 2

    :   1.  Identify and enumerate assets with at least one encryption
            tool from M1 installed (M4)
        2.  Identify and enumerate assets without at least one
            encryption tool from M1 installed (M5)

# Measures

-   M1 = Count of authorized encryption tools requiring secondary
    authentication systems
-   M2 = Count of enterprise assets storing sensitive data
-   M3 = Count of assets with at least one encryption tool installed
-   M4 = Count of assets without at least one encryption tool installed

# Metrics

## Coverage

+-----------------+----------------------------------------+---------+
| **Metric**      | | The percentage of assets storing     | | tool. |
|                 |   sensitive data covered by an         |         |
|                 |   encryption                           |         |
+-----------------+----------------------------------------+---------+
| **Calculation** | `M3 / M2`                              |         |
+-----------------+----------------------------------------+---------+
