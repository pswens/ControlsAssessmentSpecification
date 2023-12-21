## 13.5: Manage Access Control for Remote Assets

Manage access control for assets remotely connecting to enterprise
resources. Determine the amount of access to enterprise resources based on:
up-to-date anti-malware software installed, configuration compliance
with the enterprise's secure configuration process and ensure the
operating system and applications are up-to-date.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Devices      | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process
-   Safeguard 6.6: Establish and Maintain an Inventory of Authentication
    and Authorization Systems

### Inputs

1.  `GV23`: Authentication and Authorization System Inventory
2.  `GV3`: Configuration Standard
3.  `GV39`: Remote enterprise assets

### Operations

1.  Use Input 1 `GV23` to identify and enumerate authorization systems
    that allow remote logins (M1)

2.  For each authorization system identified in Operation 1, use Input 2 `GV3` to check if the configuration for each type of policy

    1.  Identify and enumerate authorization systems properly configured for all the policies (M2)
    2.  Identify and enumerate authorization systems for which at least one configuration does not comply with the policies (M3)

3.  For each remote enterprise asset from Input 3 `GV39`, compared to the output of Operation 2.1

    1.  Identify and enumerate assets that are covered by at least one compliant authorization system (M4)
    2.  Identify and enumerate assets that are not covered by a compliant authorization system (M5)

### Measures

-   M1 = Count of authorization systems that allow remote logins
-   M2 = Count of authorization systems properly configured to comply
    with policies
-   M3 = Count of authorization systems not properly configured to
    comply with policies
-   M4 = Count of remote enterprise assets covered by a compliant
    authorization system
-   M5 = Count of remote enterprise assets not covered by a compliant
    authorization system
-   M6 = Count of remote enterprise assets `GV39`

### Metrics

#### Authorization System Compliance

| **Metric**      | The percentage of properly configured authorization systems that allow remote login |
|-----------------|-------------------------------------------------------------------------------------------|
| **Calculation** | `M2 / M1`                                                                  |

#### Coverage

| **Metric**      | The percentage of remote enterprise assets covered by compliant authorization systems |
|-----------------|---------------------------------------------------------------------------------------------|
| **Calculation** | `M4 / M6`                                                                                   |
