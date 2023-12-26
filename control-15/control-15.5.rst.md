## 15.5: Assess Service Providers

Assess service providers consistent with the enterprise's service
provider management policy. Assessment scope may vary based on
classification(s), and may include review of standardized assessment
reports, such as Service Organization Control 2 (SOC 2) and Payment Card
Industry (PCI) Attestation of Compliance (AoC), customized
questionnaires or other appropriately rigorous processes. Reassess
service providers annually, at a minimum, or with new and renewed
contracts.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Identify            | 3                     |

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

    1.  If the assessment scope exists, M1 = 1
    2.  If the assessment scope does not exist, M1 = 0

2.  Use Input 1 `GV44` to determine if each listed service provider has monitoring guidance included in the policy

    1.  Identify and enumerate service providers with monitoring guidance (M3)
    2.  Identify and enumerate service providers without monitoring guidance (M4)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of service providers in inventory
-   M3 = Count of service providers with monitoring guidance
-   M4 = Count of service providers without monitoring guidance

### Metrics

-   If M1 is a 0, this safeguard receives a failing score. The other
    metrics don\'t apply.

#### Compliance

| **Metric**      | The percentage of service providers with monitoring guidance included in policy |
|-----------------|------------------------------------------------------------------------------------|
| **Calculation** | `M3 / M2`                                                                          |

