## 16.8: Separate Production and Non-Production Systems

Maintain separate environments for production and non-production
systems.

| Asset Type     | Security Function   | Implementation Groups |
| -------------- | ------------------- | --------------------- |
| Applications   | Protect             | 2, 3                  |


### Dependencies

-   None

### Inputs

1.  `GV1`: Enterprise Asset Inventory

### Operations

1.  Use Input 1 `GV1` to identify and enumerate production systems (M1)

2.  For each production system identified in Operation 1, use Input 1 `GV1` to identify if at least one non-production system exists for the system

    1.  Identify and enumerate production systems with at least one non-production system (M2)
    2.  Identify and enumerate production systems without a non-production system (M3)

### Measures

-   M1 = Count of production systems
-   M2 = Count of production systems with a non-production system to
    complement
-   M3 = Count of production systems without a non-production system to
    complement

### Metrics

#### Coverage

| **Metric**      | The percentage of non-production systems with an existing production system |
|-----------------|-----------------------------------------------------------------------------|
| **Calculation** | `M2 / M1`                                                            |

