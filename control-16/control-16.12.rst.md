## 16.12: Implement Code-Level Security Checks

Apply static and dynamic analysis tools within the application life
cycle to verify that secure coding practices are being followed.

| Asset Type     | Security Function   | Implementation Groups |
| -------------- | ------------------- | --------------------- |
| Applications   | Protect             | 3                     |

### Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory

### Inputs

1.  `GV5`: Authorized Software Inventory

### Operations

1.  Use Input 1 `GV5` to identify and enumerate in-house developed software (M1)

2.  Use Input 1 `GV5` to identify static analysis tools

3.  For each software identified in Operation 1, determine if it is verified by a static tool identified in Operation 2

    1.  Identify and enumerate software verified by a static tool (M2)
    2.  Identify and enumerate software not verified by a static tool (M3)

4.  Use Input 1 `GV5` to identify dynamic analysis tools

5.  For each software identified in Operation 1, determine if it is verified by a dynamic tool identified in Operation 4

    1.  Identify and enumerate software verified by a dynamic tool (M4)
    2.  Identify and enumerate software not verified by a dynamic tool (M5)

### Measures

-   M1 = Count of in-house developed software
-   M2 = Count of in-house developed software verified by a static
    analysis tool
-   M3 = Count of in-house developed software not verified by a static
    analysis tool
-   M4 = Count of in-house developed software verified by a dynamic
    analysis tool
-   M5 = Count of in-house developed software not verified by a dynamic
    analysis tool

## Metrics

#### Static Analysis Tool Coverage

| **Metric**      | The percentage of in-house developed software verified by a static analysis tool |
|-----------------|------------------------------------------------------------------------------------|
| **Calculation** | `M2 / M1`                                                                      |


#### Dynamic Analysis Tool Coverage

| **Metric**      | The percentage of in-house developed software verified by a dynamic analysis tool |
|-----------------|--------------------------------------------------------------------------------------|
| **Calculation** | `M4 / M1`                                                                        |
