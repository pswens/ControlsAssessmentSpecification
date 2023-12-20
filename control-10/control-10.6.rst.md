## 10.6: Centrally Manage Anti-Malware Software

Centrally manage anti-malware software.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Devices      | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 10.1: Deploy and Maintain Anti-Malware Software

### Inputs

1.  `GV30`: Assets capable of supporting anti-malware software
2.  `GV31`: Authorized anti-malware software

### Operations

1. For each authorized anti-malware software `GV31`, check if it is centrally managed

    1.  Identify and enumerate anti-malware software that is centrally managed (M2)
    2.  Identify and enumerate anti-malware software that is not centrally managed (M3)

### Measures

-   M1 = Count of `GV31`
-   M2 = Count of authorized anti-malware software that is centrally
    managed
-   M3 = Count of authorized anti-malware software that is not centrally
    managed

### Metrics

#### Coverage

| **Metric**      | The percentage of anti-malware centrally managed |
|-----------------|------------------------------------------------|
| **Calculation** | `M2 / M1`                                   |
