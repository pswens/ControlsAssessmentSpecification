# 10.7: Use Behavior-Based Anti-Malware Software

Use behavior-based anti-malware software.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Devices      Detect              2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized sofware inventory
3.  `GV3`: Configuration standards

## Operations

1.  Use `GV1` to identify and enumerate assets capable of supporting
    behavior-basaed anti-malware software (M1)

2.  Use `GV5` to identify authorized behavior-basaed anti-malware
    software

3.  

    For each asset identified in Operation 1, use the output of Operation 2

    :   1.  Identify and enumerate assets with at least one authorized
            behavior-based anti-malware software intalled (M2)
        2.  Identify and enumerate assets without any behavior-based
            anti-malware software installed (M3)

4.  

    For each asset wih a least one authorized behavior-based anti-malware software installed from Operation 3.1, use `GV3` to check configurations

    :   1.  Identify and enumerate assets with properly configured
            behavior-based anti-malware software (M4)
        2.  Identify and enumerate assets with improperly configured
            behavor-based anti-malware software (M5)

## Measures

-   M1 = Count of assets capable of supporting behavor-based
    anti-malware software
-   M2 = Count of assets with at least one authorized behavior-based
    anti-malware software installed
-   M3 = Count of assets without any behavior-based anti-malware
    software installed
-   M4 = Count of assets with properly configured authorized
    behavior-based anti-malware software installed
-   M5 = Count of assets with improperly configured authorized
    behavior-based anti-malware software installed

## Metrics

### Coverage

+-----------------+------------------------+------------------------+
| **Metric**      | | The percentage of    | | behavior-based       |
|                 |   assets with properly |   anti-malware         |
|                 |   configured           |   installed            |
|                 |   authorized           |                        |
+-----------------+------------------------+------------------------+
| **Calculation** | `M4 / M1`              |                        |
+-----------------+------------------------+------------------------+
