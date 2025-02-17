## 16.6: Establish and Maintain a Severity Rating System and Process for Application Vulnerabilities

Establish and maintain a severity rating system and process for application
vulnerabilities that facilitate prioritizing the order in which
discovered vulnerabilities are fixed. This process includes setting a
minimum level of security acceptability for releasing code or
applications. Severity ratings bring a systematic way of triaging
vulnerabilities that improves risk management and helps ensure the most
severe bugs are fixed first. Review and update the system and process
annually.

| Asset Type     | Security Function   | Implementation Groups |
| -------------- | ------------------- | --------------------- |
| Applications   | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 16.2: Establish and Maintain a Process to Accept and
    Address Software Vulnerabilities

### Inputs

1.  `GV48`: Process to Accept and Address Software Vulnerabilities
2.  Date of last update or review of the severity rating system and
    process

# Operations

1.  Using Input 1 `GV48`\` determine whether the enterprise has a severity rating system and process for application vulnerabilities

    1.  If the system and process exist, M1 = 1
    2.  If the system and process do not exist, M1 = 0

2.  Review Input 1 `GV48` and determine whether it includes, at a minimum, the following components: guidance for prioritizing the order vulnerabilities are fixed, level of security acceptability for releasing code or applications

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
|-----------------|--------------------------------------------------------------------------------------|
| **Calculation** | `M2 / 2`                                                                      |

