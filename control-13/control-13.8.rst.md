## 13.8: Deploy a Network Intrusion Prevention Solutions

Deploy a network intrusion prevention solution where appropriate.
Example implementations include the use of a Network Intrusion
Prevention System (NIPS) or equivalent CSP service.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Network      | Protect             | 3                     |

### Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 12.4: Establish and Maintain Architecture Diagram(s)

### Inputs

1.  `GV35`: Assets that are part of the network infrastructure
2.  `GV40`: Network Boundaries

### Operations

1.  Use Input 1 `GV35` to identify the network intrusion prevention
    solutions for the enterprise

2.  For each network boundary identified in Input 2, determine whether it is covered by at least one network intrusion prevention solution

    1.  Identify and enumerate boundaries covered by at least one network intrusion prevention solution (M2)
    2.  Identify and enumerate boundaries not covered by at least one network intrusion prevention solution (M3)

### Measures

-   M1 = Count of network boundaries `GV40`
-   M2 = Count of network boundaries covered by a network intrusion
    prevention solution
-   M3 = Count of network boundaries not covered by a network intrusion
    prevention solution

### Metrics

#### Coverage

| **Metric**      | The percentage of network boundaries covered by network intrusion prevention solutions |
|-----------------|------------------------------------------------------------------------------------------|
| **Calculation** | `M2 / M1`                                                                                |
