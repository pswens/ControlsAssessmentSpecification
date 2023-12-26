## 15.3: Classify Service Providers

Classify service providers. Classification considerations may include one
or more characteristics, such as data sensitivity, data volume,
availability requirements, applicable regulations, inherent risk, and
mitigated risk. Update and review classifications annually or when
significant enterprise changes occur that could impact this Safeguard.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Identify            | 2, 3                  |


### Dependencies

-   Safeguard 15.1: Establish and Maintain an Inventory of Service
    Providers
-   Safeguard 15.2: Establish and Maintain a Service Provider Management
    Policy

### Inputs

1.  `GV44`: Service Provider Inventory List
2.  `GV45`: Service Provider Management Policy
3.  `GV46`: Date of last review or update to service provider inventory

### Operations

1. Use Input 2 `GV45` to determine if the enterprise policy includes the classification process of service providers by one or more characteristics

    1.  If the process exists, M1 = 1
    2.  If the process does not exist, M1 = 0

2.  Compare the date of Input 3 `GV46` to the current date and capture timeframe in months (M2)

3.  Review Input 1 `GV45` and determine whether service providers are classified using one or more characteristics per the enterprise\'s policy

    1.  Identify and enumerate service providers with an assigned classification (M4)
    2.  Identify and enumerate service providers without a classification (M5)

### Measures

-   M1 = Output of Operation 1
-   M2 = Timeframe since the last update or review of the service provider
    inventory
-   M3 = Count of service providers in inventory
-   M4 = Count of service providers with classification
-   M5 = Count of service providers without classification

## Metrics

-   If M1 is a 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M2 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

### Coverage

| **Metric**      | The percentage of service providers with a classification |
|-----------------|----------------------------------------------------------|
| **Calculation** | `M4 / M3`                                                |

