## 16.4: Establish and Manage an Inventory of Third-Party Software Components

Establish and manage an updated inventory of third-party components used
in development, often referred to as a "bill of materials," as well as
components slated for future use. This inventory is to include any risks
that each third-party component could pose. Evaluate the list at least
monthly to identify any changes or updates to these components and
validate that the component is still supported. 

| Asset Type     | Security Function   | Implementation Groups |
| -------------- | ------------------- | --------------------- |
| Applications   | Protect             | 2, 3                  |


### Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory

### Inputs

1.  `GV47`: Inventory of Third-Party Software Components
2.  Date of last review or update of the inventory

### Operations

1.  Determine whether Input 1 exists within the enterprise

    1.  If Input 1 exists, M1 = 1
    2.  If Input 1 does not exist, M1 = 0

2.  Use Input 1 and determine whether each software component listed includes, at a minimum, the following information: risk associated with components, whether the component is supported

    1.  Identify and enumerate software components with complete information (M3)
    2.  Identify and enumerate software components with missing information (M4)

3.  Compare the date of Input 2 to the current date and capture the timeframe in days (M5)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of Input 1
-   M3 = Count of software components with complete information
-   M4 = Count of software components with missing information
-   M5 = Timeframe since the last review or update of the inventory

### Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M5 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

#### Completeness of Inventory

| **Metric**      | The percent of components included in the secure application development process |
|-----------------|-----------------------------------------------------------------------------------|
| **Calculation** | `M3 / M2`                                                                   |

