## 14.5: Train Workforce Members on Causes of Unintentional Data Exposure

Train workforce members to be aware of causes for unintentional data exposure.
Example topics include the miss-delivery of sensitive data, losing a portable
end-user device, or publishing data to unintended audiences.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Protect             | 1, 2, 3               |

### Dependencies

-   None

### Inputs

1.  Causes of Unintentional Data Exposure training module
2.  `GV43`: List of workforce members
3.  List of most recent module training completion dates for each
    workforce member

### Operations

1.  Check enterprise to determine if Input 1 exists

    1.  If Input 1 exists, M1 = 1
    2.  2.  If Input 1 does not exist, M1 = 0

2.  For every member of the workforce in Input 2 `GV43`, determine whether the member has completed training

    1.  Identify and enumerate members who have completed at least initial training (M3)
    2.  Identify and enumerate members who have not completed any training (M4)

3.  For every member of the workforce identified in Operation 2.1,
    identify the date of most recently completed module training

4.  For every member of the workforce identified in Operation 2.1, use the output of Operation 4 and compare the date to the current date. Capture timeframe in months.

     1.  Identify and enumerate members whose most recent training date is less than or equal to twelve months from the current date (M5)
     2.  Identify and enumerate members whose most recent training date is greater than twelve months from the current date (M6)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of Input 1 `GV43`
-   M3 = Count of workforce members that have completed training
-   M4 = Count of workforce members that have not completed training
-   M5 = Count of workforce members whose training is up to date
-   M6 = Count of workforce members whose training is not up to date

### Metrics

-   If M1 is measured at a 0, this safeguard receives a failing score.
    The other metrics don\'t apply.

#### Initial Training Compliance

| **Metric**      | The percentage of workforce members that have received initial training |
|-----------------|------------------------------------------------------------------------|
| **Calculation** | `M2 / M1`                                                              |


#### Up to Date Training

| **Metric**      | The percentage of compliant workforce members |
|-----------------|------------------------------------------------|
| **Calculation** | `M4 / M1`                                      |

