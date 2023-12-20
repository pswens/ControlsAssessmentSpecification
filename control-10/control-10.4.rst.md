## 10.4: Configure Automatic Anti-Malware Scanning of Removable Media

Configure anti-malware software to automatically
scan removable media.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Devices      | Detect              | 2, 3                  |

## Dependencies

-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process
-   Safeguard 10.1: Deploy and Maintain Anti-Malware Software

## Inputs

1.  `GV30`: Assets capable of supporting anti-malware software
2.  `GV32`: Assets with at least one authorized anti-malware software installed
3.  `GV3`: Configuration standards

## Operations

1. For each asset in Input 2 `GV32`, use configurations `GV3` to identify if the software is configured to automatically scan removable media

    1.  Identify and enumerate assets with properly configured software (M2)
    2.  Identify and enumerate assets with improperly configured software (M3)

## Measures

-   M1 = Count of `GV30`
-   M2 = Count of assets with anti-malware properly configured to scan
    removable media
-   M3 = Count of assets with anti-malware not properly configured to
    scan removable media

## Metrics

### Coverage

| **Metric**      | The percentage of assets with properly configured software to automatically scan removable media |
|-----------------|--------------------------------------------------------------------------------------------------------|
| **Calculation** | `M2 / M1`                                                                                   |

