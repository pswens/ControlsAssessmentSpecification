## 10.2: Configure Automatic Anti-Malware Signature Updates

Configure automatic updates for anti-malware signature files on all enterprise assets.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Devices      | Protect             | 1, 2, 3               |

### Dependencies

-   Safeguard 10.1: Deploy and Maintain Anti-Malware Software

### Inputs

1.  `GV30`: Assets capable of supporting anti-malware software
2.  `GV31`: Assets with at least one authorized anti-malware software installed
3.  `GV3`: Configuration standards

### Operations

1.  For each asset in Input 2 `GV31`, check configurations `GV3` to determine if anti-malware software is configured to autmatically update signature files

    1.  Identify and enumerate assets properly configured for automatic updates (M2)
    2.  Identify and enumerate assets not properly configured for automatic updates (M3)

### Measures

-   M1 = Count of `GV30`
-   M2 = Count of assets configured to automatically update signature
    files
-   M3 = Count of assets not configured to automatically update
    signature files

### Metrics

#### Coverage

| **Metric**      | The percentage of assets properly configured to automatically update signature files |
|-----------------|---------------------------------------------------------------------------------------|
| **Calculation** | `M2 / M1`                                                                      |

