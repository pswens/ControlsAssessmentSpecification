## 17.1: Designate Personnel to Manage Incident Handling

Designate one key person and at least one backup who will manage the enterprise's incident-handling
process. Management personnel are responsible for the coordination and
documentation of incident response and recovery efforts and can consist
of employees internal to the enterprise, third-party vendors, or a
hybrid approach. If using a third-party vendor, designate at least one
person internal to the enterprise to oversee any third-party work.
Review annually or when significant enterprise changes occur that could
impact this Safeguard.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Respond             | 1, 2, 3               |

### Dependencies

-   None

### Inputs

1.  `GV51`: Enterprise Incident Response Documentation
2.  Date of last update or review of the documentation

### Operations

1.  Determine whether the enterprise documents designated personnel to manage incident handling by reviewing Input 1 `GV51`. Input 1 can be an incident response plan or other documentation.

    1.  If documentation designating personnel exists, M1 = 1
    2.  If documentation designating personnel does not exist, M1 = 0

2.  Determine whether the documentation, at a minimum, outlines the following components: primary personnel, backup personnel, roles and responsibilities of each

    1.  For each component included, assign a value of 1. Sum the values. (M2)

3.  Compare Input 2 to the current date and capture the timeframe in months (M3)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of components included for designated personnel
    documentation
-   M3 = Timeframe since the last update or review of documentation in
    months

### Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M3 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

#### Completeness

| **Metric**      | The percentage of components included in the documentation for designated incident handling personnel |
|-----------------|--------------------------------------------------------------------------------------------------|
| **Calculation** | `M2 / 3`                                                                                  |
