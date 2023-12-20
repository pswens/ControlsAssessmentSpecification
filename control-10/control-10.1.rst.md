## 10.1: Deploy and Maintain Anti-Malware Software

Deploy and maintain anti-malware software on all enterprise assets.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Devices      Protect             1, 2, 3

### Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

### Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized sofware inventory
3.  `GV3`: Configuration standards

### Operations

1.  Use `GV1` to identify and enumerate assets capable of supporting
    anti-malware software: `GV30` (M1)

2.  Use `GV5` to identify authorized anti-malware software: `GV31`

3.  For each asset identified in Operation 1, use the output of Operation 2

    1.  Identify and enumerate assets with at least one authorized anti-malware software intalled: `GV32` (M2)
    2.  Identify and enumerate assets with only unauthorized anti-malware software installed (M3)
    3.  Identify and enumerate assets without any anti-malware software installed (M4)

4. For each asset with a least one authorized anti-malware software installed from Operation 3.1, use `GV3` to check configurations

    1.  Identify and enumerate assets with properly configured anti-malware software (M5)
    2.  Identify and enumerate assets with improperly configured anti-malware software (M6)

### Measures

-   M1 = Count of assets capable of supporting anti-malware software
-   M2 = Count of assets with at least one authorized anti-malware
    software installed
-   M3 = Count of assets with only unauthorized anti-malware software
    installed
-   M4 = Count of assets without any anti-malware software installed
-   M5 = Count of assets with properly configured authorized
    anti-malware software installed
-   M6 = Count of assets with improperly configured authorized
    anti-malware software installed

### Metrics

#### Coverage

+-----------------+------------------------+------------------------+
| **Metric**      | | The percentage of    | | anti-malware         |
|                 |   assets with properly |   installed            |
|                 |   configured           |                        |
|                 |   authorized           |                        |
+-----------------+------------------------+------------------------+
| **Calculation** | `M5 / M1`              |                        |
+-----------------+------------------------+------------------------+
