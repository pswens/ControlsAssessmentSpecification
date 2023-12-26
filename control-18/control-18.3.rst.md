## 18.3: Remediate Penetration Test Findings

Remediate penetration test findings based on the enterprise's policy for
remediation scope and prioritization.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Network      | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 18.2: Perform Periodic External Penetration Tests

### Inputs

1.  :code:\`GV53: Penetration Testing Program Documentation
2.  `GV54`: Most Recent External Penetration Report
3.  External penetration report prior to most recent report

### Operations

1.  Use the findings in Input 3 to identify and enumerate the
    vulnerabilities outlined (M1)

2.  Use the findings in Input 2 `GV54` to identify the vulnerabilities
    outlined

3.  Compare the output of Operation 1 and Operation 1

    1.  Identify and enumerate vulnerabilities found in Input 3 that continue to be in Input 2 (M2)
    2.  Identify and enumerate vulnerabilities found in Input 3 that no longer appear in Input 2 (M3)

4.  Using the program documentation from Input 1 `GV53`, determine whether the output of Operation 3.2 is still within scope based on enterprise\'s policy

    1.  Identify and enumerate vulnerabilities within scope (M4)
    2.  Identify and enumerate vulnerabilities out of scope (M5)

### Measures

-   M1 = Count of initial vulnerabilities identified by a penetration test
-   M2 = Count of successfully remediated vulnerabilities
-   M3 = Count of vulnerabilities that have not been remediated
-   M4 = Count of unremediated vulnerabilities still in scope
-   M5 = Count of unremediated vulnerabilities out of scope

### Metrics

#### Compliance

| **Metric**      | The percent of successfully remediated or still within scope vulnerabilities identified in the initial penetration test findings. |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Calculation** | `(M3 + M4) / M1`                                                                                                                        |

