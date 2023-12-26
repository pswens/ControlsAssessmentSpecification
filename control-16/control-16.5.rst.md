## 16.5: Use Up-to-Date and Trusted Third-Party Software Components

Use up-to-date and trusted third-party software components. When
possible, choose established and proven frameworks and libraries that
provide adequate security. Acquire these components from trusted sources
or evaluate the software for vulnerabilities before use.

| Asset Type     | Security Function   | Implementation Groups |
| -------------- | ------------------- | --------------------- |
| Applications   | Protect             | 2, 3                  |


### Dependencies

-   Safeguard 16.4: Establish and Manage an Inventory of Third-Party
    Software Components

### Inputs

1.  `GV47`: Inventory of Third-Party Software Components

### Operations

1.  For each software component in Input 1 `GV47`, determine whether the latest component is being used

    1.  Identify and enumerate software components that are up-to-date (M2)
    2.  Identify and enumerate software components that are not up-to-date (M3)

2.  For each software component identified in Operation 1.1, determine whether they are explicitly trusted by the enterprise

    1.  Identify and enumerate software components that are trusted by the enterprise (M4)

### Measures

-   M1 = Count of Input 1
-   M2 = Count of software components that are up-to-date
-   M3 = Count of software components that are not up-to-date
-   M4 = Count of software components that are up-to-date and trusted

### Metrics

#### Compliance

| **Metric**      | The percentage of up-to-date and trusted software components |
|-----------------|--------------------------------------------------------------|
| **Calculation** | `M4 / M1`                                              |

