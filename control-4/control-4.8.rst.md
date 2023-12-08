4.8: Uninstall or Disable Unnecessary Services on Enterprise Assets and
Software
================================================================
Uninstall or disable unnecessary services on enterprise assets and
software, such as an unused file sharing service, web application
module, or service function.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Devices      Protect             2, 3

# Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory

# Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized software inventory
3.  `GV3`: Configuration standard

# Operations

1.  Use `GV5` to identify and enumerate authorized services (M1)

2.  Use `GV1` to identify and enumerate services on enterprise assets
    (M2)

3.  

    Compare outputs from Operations 1 and 2

    :   1.  Identify and enumerate authorized services on assets (M3)
        2.  Identify and enumerate unauthorized services on assets (M4)

4.  

    For authorized services in Operation 3.2, use `GV3` to check configurations

    :   1.  Identify and enumerate services that are configured
            correctly (disabled) (M5)
        2.  Identify and enumerate services that are configured
            improperly (enabled) (M6)

# Measures

-   M1 = Count of authorized services
-   M2 = Count of services on enterprise assets
-   M3 = Count of authorized services on assets
-   M4 = Count of unauthorized services on assets
-   M5 = Count of unauthorized services that are disabled
-   M6 = Count of unauthorized serivces that are enabled

# Metrics

## Compliant Services

+-----------------+---------------------------------------------------------+
| **Metric**      | | The percentage of services installed/running that are |
|                 | | enterprise essential                                  |
+-----------------+---------------------------------------------------------+
| **Calculation** | `(M3 + M5) / M2`                                        |
+-----------------+---------------------------------------------------------+

## Non-compliant Services

> -   -   **Metric**
>
>     -   | The percentage of services installed/running that are
>         | not enteprise essential
>
> -   -   **Calculation**
>     -   `M6 / M2`
