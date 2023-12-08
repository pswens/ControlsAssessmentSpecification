# 10.5: Enable Anti-Exploitation Features

Enable anti-exploitation features on enterprise assets and software,
where possible, such as Microsoft® Data Execution Prevention (DEP),
Windows® Defender Exploit Guard (WDEG), or Apple® System Integrity
Protection (SIP) and Gatekeeper™.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Devices      Protect             2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standards

## Operations

1.  

    For each asset in `GV1`, use configuration standards `GV3` to determine if it is propely configured to enable anti-exploitation features

    :   1.  Identify and enumerate assets properly configured to enable
            anti-exploitation features (M2)
        2.  Identify and enumerate assets not properly configured to
            enable anti-exploitation features (M3)

## Measures

-   M1 = Count of `GV1`
-   M2 = Count of assets properly configured to enable anti-exploitation
    feautures
-   M3 = Count of assets not properly configured to enable
    anti-exploitation features

## Metrics

### Coverage

+-----------------+------------------------+------------------------+
| **Metric**      | | The percentage of    | | anti-exploitation    |
|                 |   assets properly      |   features.            |
|                 |   configured to enable |                        |
+-----------------+------------------------+------------------------+
| **Calculation** | `M2 / M1`              |                        |
+-----------------+------------------------+------------------------+
