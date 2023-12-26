## 18.1: Establish and Maintain a Penetration Testing Program

Establish and maintain a penetration testing program appropriate to the size,
complexity, and maturity of the enterprise. Penetration testing program
characteristics include scope, such as network, web application,
Application Programming Interface (API), hosted services, and physical
premise controls, frequency; limitations, such as acceptable hours, and
excluded attack types; point of contact information; remediation, such
as how findings will be routed internally and retrospective
requirements.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Identify            | 2, 3                  |

### Dependencies

-   None

### Inputs

1.  `GV53` Penetration Testing Program Documentation
2.  Date of last update to the penetration testing program documentation

### Operations

1.  Determine if Input 1 `GV53` exists within the enterprise

    1.  If Input 1 exists, M1 = 1
    2.  If Input 1 does not exist, M1 = 0

2.  Check Input 1 for completeness. At a minimum, it should include the scope of the program, frequency, point of contact information, remediation, and retrospective requirements.

    1.  For each component included in the documentation, assign a value of 1. Sum the values. (M2)

3.  Compare Input 2 to the current date. Capture timeframe in months (M3)

### Measures

-   M1 = Output of Operation 1
-   M2 = Sum of components included in the documentation
-   M3 = Timeframe in months since the last update to the documentation

### Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M3 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

#### Completeness

| **Metric**      | The percentage of minimum components included in the program documentation |
|-----------------|----------------------------------------------------------------------------|
| **Calculation** | `M2 / 5`                                                            |

