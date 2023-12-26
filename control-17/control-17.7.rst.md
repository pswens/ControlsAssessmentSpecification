## 17.7: Conduct Routine Incident Response Exercises

Plan and conduct routine incident response exercises and scenarios for
key personnel involved in the incident response process to prepare for
responding to real-world incidents. Exercises need to test communication
channels, decision-making, and workflows. Conduct testing on an annual
basis, at a minimum.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Recover             | 2, 3                  |


### Dependencies

-   Safeguard 17.4: Establish and Maintain an Incident Response Process

### Inputs

1.  `GV52`: Incident response process
2.  Date of last exercise or test

### Operations

1.  Determine whether the enterprise\'s incident response process includes routine incident response exercises by reviewing Input 1 `GV52`

    1.  If the documentation includes exercises, M1 = 1
    2.  If the documentation does not include exercises, M1 = 0

2.  Determine whether the documentation for exercises, at a minimum, outlines test communication channels, decision-making, and workflows

    1.  For each mechanism included, assign a value of 1. Sum the values. (M2)

3.  Compare Input 2 to the current date and capture the timeframe in months (M3)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of components included in the documentation
-   M3 = Timeframe since the last exercise or test in months

### Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M3 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

#### Completeness

| **Metric**      | The percentage of components included in documentation for incident response exercises |
|-----------------|------------------------------------------------------------------------------------------|
| **Calculation** | `M2 / 3`                                                                          |

