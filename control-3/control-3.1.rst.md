## 3.1: Establish and Maintain a Data Management Process

Establish and maintain a data management process. In the process, address data sensitivity, data owner, handling of data, data retention limits, and disposal requirements based on sensitivity and retention standards for the enterprise. Review and update documentation annually, or when significant enterprise changes occur, that could impact this Safeguard.

| Asset Type   | Security Function | Implementation Groups |
|--------------|-------------------|------------------------|
| Applications | Identify          | 1, 2, 3                |

### Dependencies

-   None

### Inputs

1.  `GV10`: Enterprise\'s data management process
2.  Date of last update to the data management process

### Operations

1. Review `GV10` to determine if, at a minimum, it includes:
   
  1. Addressing data sensitivity. If so, M1 = 1. Otherwise M1 = 0. (`GV11`)
  2. Captures data owner. If so, M2 = 1. Otherwise M2 = 0. (`GV13`)
  3. Handling of data. If so, M3 = 1. Otherwise, M3 = 0. (`GV14`)
  4. Data retention limits based on the sensitivity of data. If so, M4 = 1. Otherwise, M4 = 0. (`GV15`)
  5. Disposal requirements based on the sensitivity of data. If so, M5 = 1. Otherwise, M5 = 0. (`GV16`)

### Measures

-   M1 = Does the process address data sensitivity
-   M2 = Does the process capture data owners
-   M3 = Does the process include guidance for handling of data
-   M4 = Does the process include data retention limits based on
    sensitivity of data
-   M5 = Does the process include guidance on disposal requirements
    based on the sensitivity of data
-   M6 = `GV10`

### Metrics

-   If M6 is not available or does not exist, this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

#### Completeness of Data Management Process

| **Metric**      | The percentage of completeness for the enterprise's data management process.                  |
| :-------------- | :----------------------------------------------------------------------------------------------- |
| **Calculation** | `(M1 + M2 + M3 + M4 + M5) / 5`                                                           |

