## 16.2: Establish and Maintain a Process to Accept and Address Software Vulnerabilities

Establish and maintain a process to accept and address reports of software
vulnerabilities, including providing a means for external entities to
report. The process includes such items as a vulnerability
handling policy that identifies the reporting process, the responsible party for
handling vulnerability reports, and a process for intake, assignment,
remediation, and remediation testing. As part of the process, use a
vulnerability tracking system that includes severity ratings and
metrics for measuring timing for identification, analysis, and
remediation of vulnerabilities. Review and update documentation
annually or when significant enterprise changes occur, that could impact
this Safeguard.

Third-party application developers need to consider this an
externally-facing policy that helps to set expectations for outside
stakeholders.

| Asset Type     | Security Function   | Implementation Groups |
| -------------- | ------------------- | --------------------- |
| Applications   | Protect             | 2, 3                  |

### Dependencies

-   None

### Inputs

1.  `GV48`: Process to Accept and Address Software Vulnerabilities
2.  Date of last update or review of process

### Operations

1. Determine whether Input 1 exists within the enterprise

    1.  If Input 1 exists, M1 = 1
    2.  If Input 1 does not exist, M1 = 0

2. Review Input 1 `GV48` and determine whether it includes, at a minimum, the following components: a reporting process, a responsible party for handling vulnerability reports, a process for intake, assignment, remediation, remediation testing, and a vulnerability tracking system

    1.  For each component included in the process, assign a value of 1. Sum all values. (M2)

3.  Compare Input 2 to the current date and capture the timeframe in months (M3)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of components included in the process
-   M3 = Timeframe in months since last review or update

### Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M3 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

#### Completeness

| **Metric**      | The percentage of components included in the secure application development process |
|-----------------|-------------------------------------------------------------------------------------|
| **Calculation** | `M2 / 7`                                                                     |

