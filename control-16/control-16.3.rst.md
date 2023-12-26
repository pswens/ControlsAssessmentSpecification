## 16.3: Perform Root Cause Analysis on Security Vulnerabilities

Perform root cause analysis on security vulnerabilities. When reviewing
vulnerabilities, root cause analysis is the task of evaluating
underlying issues that create vulnerabilities in code and allows
development teams to move beyond just fixing individual vulnerabilities
as they arise.

| Asset Type     | Security Function   | Implementation Groups |
| -------------- | ------------------- | --------------------- |
| Applications   | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 16.2: Establish and Maintain a Process to Accept and
    Address Software Vulnerabilities

### Inputs

1.  Root Cause Analysis Process
2.  Vulnerabilities addressed over the last twelve months

### Operations

1.  Determine whether Input 1 exists within the enterprise

    1.  If Input 1 exists, M1 = 1
    2.  If Input 1 does not exist, M1 = 0

2.  Review Input 1 and determine whether it includes, at a minimum, the following components: categorization of vulnerabilities, guidance for how lessons learned are incorporated into the development process

    1.  For each component included in the process, assign a value of 1. Sum all values. (M2)

3.  For each vulnerability addressed over the last twelve months, assess whether the root cause analysis process was followed

    1.  Identify and enumerate vulnerabilities for which the process was followed (M4)
    2.  Identify and enumerate vulnerabilities for which the process was not followed (M5)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of components included in the process
-   M3 = Count of Input 2
-   M4 = Count of vulnerabilities for which root cause analysis was
    conducted
-   M5 = Count of vulnerabilities for which root cause analysis was not
    conducted

### Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.

#### Completeness of Process

| **Metric**      | The percentage of components included in the secure application development process |
|-----------------|-------------------------------------------------------------------------------------|
| **Calculation** | `M2 / 2`                                                                     |


#### Compliance

| **Metric**      | The percentage of vulnerabilities for which root cause analysis was conducted |
|-----------------|-----------------------------------------------------------------------------|
| **Calculation** | `M4 / M3`                                                             |

