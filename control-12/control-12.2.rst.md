## 12.2: Establish and Maintain a Secure Network Architecture

Establish and maintain a secure network architecture. A secure network
architecture must address segmentation, least privilege, and
availability, at a minimum.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Network      | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 12.4: Establish and Maintain Architecture Diagram(s)
-   Safeguard 2.1: Establish and Maintain a Software Inventory

### Inputs

1.  `GV4`: Enterprise network architecture documentation
2.  `GV5`: Authorized software inventory

### Operations

1.  Use the network architecture `GV4` to identify and enumerate the segments within the enterprise network `GV36` (M1)

2.  For each network segment identified in Operation 1, attempt to connect an unauthorized device

    1.  Identify and enumerate segments that allow you to connect unauthorized devices (M2)
    2.  Identify and enumerate segments that do not allow you to connect unauthorized devices (M3)

3.  Use `GV5` to identify authorized availability monitoring software

4.  For each network segment identified in Operation 1, determine whether an authorized availability monitoring software from Operation 3 covers the segment

    1.  Identify and enumerate segments that are covered by availability monitoring software (M4)
    2.  Identify and enumerate segments that are not covered by availability monitoring software (M5)

### Measures

-   M1 = Count of network segments within the enterprise
-   M2 = Count of segments not compliant with least privilege
-   M3 = Count of segments compliant with least privilege
-   M4 = Count of segments monitored for availability
-   M5 = Count of segments not monitored for availability

### Metrics

#### Segmentation

| **Metric**      | If M1 is equal to 1, this metric is measured at a 0. Subsequent metrics can still be assessed. |
|-----------------|---------------------------------------------------------------------------------------------|
| **Calculation** | `If M1 <= 1, Fail or If M1 >= 1, Pass`                                               |

#### Least Privilege

| **Metric**      | The percentage of network segments implementing least privilege |
|-----------------|--------------------------------------------------------------|
| **Calculation** | `M3 / M1`                                              |


#### Availability

| **Metric**      | The percentage of network segments monitored for network availability |
|-----------------|--------------------------------------------------------------------|
| **Calculation** | `M4 / M1`                                                    |

