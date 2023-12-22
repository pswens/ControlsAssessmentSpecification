## 13.10: Perform Application Layer Filtering

Perform application layer filtering. Example implementations include a
filtering proxy, application layer firewall, or gateway.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Network      | Protect             | 3                     |

### Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory

## Inputs

1.  `GV35`: Assets that are part of the network infrastructure
2.  `GV5`: Authorized Software Inventory

### Operations

1.  Use Input 2 `GV5` to identify software used for application layer filtering

2.  For each asset in Input 1 `GV35, determine whether it is covered by at least one software identified in Operation 1

    1.  Identify and enumerate assets covered by application layer filtering software (M2)
    2.  Identify and enumerate assets not covered by application layer filtering software (M3)

### Measures

-   M1 = Count of network infrastructure assets
-   M2 = Count of network infrastructure assets covered by the application
    layer filtering software
-   M3 = Count of network infrastructure assets not covered by
    application layer filtering software

### Metrics

### Coverage

| **Metric**      | The percentage of network infrastructure assets covered by application layering software |
|-----------------|-------------------------------------------------------------------------------------------|
| **Calculation** | `M2 / M1`                                                                                 |
