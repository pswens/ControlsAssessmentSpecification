## 18.5: Perform Periodic Internal Penetration Tests

Perform periodic internal penetration tests based on program
requirements, no less than annually. The testing may be a clear box or
an opaque box.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Identify            | 3                     |

### Dependencies

-   Safeguard 18.1: Establish and Maintain a Penetration Testing Program

### Inputs

1.  `GV55`: Most Recent Internal Penetration Report

### Operations

1.  Check Input 1 `GV55` for the date of the most recent internal penetration
    test. Compare the date to the current date and capture the timeframe in months
    (M1)

### Measures

-   M1 = Timeframe since the last internal penetration test

### Metrics

-   If M1 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.
