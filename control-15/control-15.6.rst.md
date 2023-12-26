## 15.6: Monitor Service Providers

Monitor service providers consistent with the enterprise's service
provider management policy. Monitoring may include periodic reassessment
of service provider compliance, monitoring service provider release
notes, and dark web monitoring.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Data         | Detect              | 3                     |


### Dependencies

-   Safeguard 15.1: Establish and Maintain an Inventory of Service
    Providers
-   Safeguard 15.2: Establish and Maintain a Service Provider Management
    Policy

### Inputs

1.  `GV44`: Service Provider Inventory List
2.  `GV45`: Service Provider Management Policy

### Operations

1.  Use Input 2 `GV45` to determine if the enterprise policy includes monitoring guidance for service providers

    1.  If the monitoring guidance exists, M1 = 1
    2.  If the monitoring guidance does not exist, M1 = 0

2.  Use Input 1 `GV44` to determine if each listed service provider has monitoring guidance provided in the policy

    1.  Identify and enumerate service providers with monitoring guidance provided (M3)
    2.  Identify and enumerate service providers without monitoring guidance provided (M4)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of service providers in inventory
-   M3 = Count of service providers with monitoring guidance provided
-   M4 = Count of service providers without monitoring guidance provided

### Metrics

-   If M1 is a 0, this safeguard receives a failing score. The other
    metrics don\'t apply.

#### Compliance

| **Metric**      | The percentage of service providers with up-to-date assessments |
|-----------------|--------------------------------------------------------------|
| **Calculation** | `M3 / M2`                                                    |

