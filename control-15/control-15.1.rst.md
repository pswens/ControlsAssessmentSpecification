## 15.1: Establish and Maintain an Inventory of Service Providers

Establish and maintain an inventory of service providers. The inventory
is to list all known service providers, including classification(s) and
designate an enterprise contact for each service provider. Review and
update the inventory annually or when significant enterprise changes
occur that could impact this Safeguard.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| N/A          | Identify            | 1, 2, 3               |

### Dependencies

-   None

### Inputs

1.  `GV44`: Service Provider Inventory List
2.  `GV46`: Date of last review or update of the service provider
    inventory

### Operations

1. Determine whether the enterprise maintains a service provider inventory list by checking for Input 1,

    1.  If Input 1 exists, M1 = 1
    2.  If Input 2 does not exist, M1 = 0

2. Review Input 1 and determine if it includes, at a minimum, the following components: service provider, classification of provider, and an enterprise contact for the provider

    1.  For each component included, assign a value of 1. Sum all values. (M2)

3.  For each service provider identified in Input 1 `GV45`, determine whether they are accurately listed

    1.  Identify and enumerate providers that are accurately listed (M4)
    2.  Identify and enumerate providers that are erroneously listed (M5)
    3.  Identify and enumerate providers that should be listed but are missing (M6)

4.  Compare the date from Input 2 with the current date and capture the time frame in months (M7)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of components included in the inventory
-   M3 = Count of service providers in the inventory
-   M4 = Count of accurately listed providers
-   M5 = Count of erroneously listed providers
-   M6 = Count of missing providers from the list
-   M7 = Timeframe since the last update or review of the inventory

### Metrics

-   If M1 is a 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M7 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

#### Completeness of Inventory

| **Metric**      | The percentage of components included in the inventory |
|-----------------|--------------------------------------------------------|
| **Calculation** | `M2 / 3`                                               |

#### Accuracy of Inventory 

| **Metric**      | The percentage of accurately listed service providers in the inventory |
|-----------------|------------------------------------------------------------------------|
| **Calculation** | :code:`M4 / (M3 - M5 + M6)`                                          |
