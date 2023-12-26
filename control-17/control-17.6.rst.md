## 17.6: Define Mechanisms for Communicating During Incident Response

Determine which primary and secondary mechanisms will be used to
communicate and report during a security incident. Mechanisms can
include phone calls, emails, or letters. Keep in mind that certain
mechanisms, such as emails, can be affected during a security incident.
Review annually or when significant enterprise changes occur that could
impact this Safeguard.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Respond             | 2, 3                  |

### Dependencies

-   Safeguard 17.4: Establish and Maintain an Incident Response Process

### Inputs

1.  `GV52`: Incident response process
2.  Date of last update or review of the documentation

### Operations

1.  Determine whether the enterprise document mechanisms for communication by reviewing Input 1 `GV52`

    1.  If the documentation for an incident response process exists, M1 = 1
    2.  If the documentation for an incident response process does not exist, M1 = 0

2.  Determine whether the documentation, at a minimum, outlines primary and secondary mechanisms for communication

    1.  For each mechanism included, assign a value of 1. Sum the values. (M2)

3.  Compare Input 2 to the current date and capture the timeframe in months (M3)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of mechanisms for communication included in the documentation
-   M3 = Timeframe since the last update or review of documentation in
    months

### Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M3 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

#### Completeness

| **Metric**      | The percentage of components included in the documentation for designated incident handling personnel |
|-----------------|----------------------------------------------------------------------------------------------------------|
| **Calculation** | `M2 / 2`                                                                                          |

