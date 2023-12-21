## 12.5: Centralize Network Authentication, Authorization, and AuCentralize network AAA.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Network      | Protect             | 2, 3                  |


## Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory

## Inputs

1.  `GV5`: Authorized Software Inventory
2.  `GV35`: Assets that are part of the network infrastructure

## Operations

1.  Use Input 1 `GV5` to identify and enumerate all AAA services within
    the enterprise `GV38` (M1)

2.  For each centralized AAA point identified in Operation 1, determine whether it is necessary or can be consolidated

    1.  Identify and enumerate authentication points that are unnecessary or can be consolidated (M2)
    2.  Identify and enumerate authentication points that are necessary and cannot be consolidated (M3)

3. Use the output of Operation 1 to check if each asset in Input 2 `GV35` is covered by at least one AAA system

    1.  Identify and enumerate network infrastructure assets that are covered by at least one AAA system (M4)
    2.  Identify and enumerate network infrastructure assets that are not covered by an AAA system (M5)

## Measures

-   M1 = Count of AAA services within the enterprise
-   M2 = Count of unnecessary AAA services
-   M3 = Count of necessary AAA services
-   M4 = Count of network infrastructure covered by AAA services
-   M5 = Count of network infrastructure not covered by AAA services
-   M6 = Count of `GV35`

## Metrics

### Centralized AAA

| **Metric**      | Percentage of properly centralized AAA services |
|-----------------|-------------------------------------------------|
| **Calculation** | `M3 / M1`                                       |


### Network Coverage

| **Metric**      | Percentage of network infrastructure assets managed through AAA |
|-----------------|-------------------------------------------------------------|
| **Calculation** | `M4 / M6`                                                   |
