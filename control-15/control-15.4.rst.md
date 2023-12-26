## 15.4: Ensure Service Provider Contracts Include Security Requirements

Ensure service provider contracts include security requirements. Example requirements
may include minimum security program requirements, security incident
and/or data breach notification and response, data encryption
requirements, and data disposal commitments. These security requirements
must be consistent with the enterprise's service provider management
policy. Review service provider contracts annually to ensure contracts
are not missing security requirements.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 15.1: Establish and Maintain an Inventory of Service
    Providers
-   Safeguard 15.2: Establish and Maintain a Service Provider Management
    Policy

### Inputs

1.  `GV44`: Service Provider Inventory List
2.  `GV45`: Service Provider Management Policy
3.  Date of last update or review of contracts

### Operations

1.  Use Input 2 `GV45` to determine if the enterprise policy includes security program requirements for service providers

    1.  If the security requirements exist, M1 = 1
    2.  If the security requirements do not exist, M1 = 0

2.  Use Input 1 `GV44` to determine if each listed service provider has a contract

    1.  Identify and enumerate service providers with contracts (M3)
    2.  Identify and enumerate service providers without contracts (M4)

3. For each service provider with a contract identified in Operation 2.1, compare the date from input 3 to the current date and capture the timeframe in months

    1.  Identify and enumerate service providers whose contract has been reviewed within twelve months or less (M5)
    2.  Identify and enumerate service providers whose contract has been reviewed outside the twelve-month window (M6)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of service providers in inventory
-   M3 = Count of service providers with contracts
-   M4 = Count of service providers without contracts
-   M5 = Count of service providers with up-to-date contracts
-   M6 = Count of service providers without outdated contracts

### Metrics

-   If M1 is a 0, this safeguard receives a failing score. The other
    metrics don\'t apply.

#### Compliance

| **Metric**      | The percentage of service providers with up-to-date contract |
|-----------------|-------------------------------------------------------------|
| **Calculation** | `M5 / M2`                                                   |

