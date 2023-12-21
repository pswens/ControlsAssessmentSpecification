## 12.6: Use of Secure Network Management and Communication Protocols 

Use secure network management and communication protocols (e.g., 802.1X, Wi-Fi
Protected Access 2 (WPA2) Enterprise or greater).

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Network      | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 4.2: Establish and Maintain a Secure Configuration Process
    for Network Infrastructure
-   Safeguard 12.2: Establish and Maintain a Secure Network Architecture

### Inputs

1.  `GV36`: Segments within the enterprise network
2.  `GV37`: Network infrastructure configuration standards
3.  Authorized list of secure network management and communication
    protocols

### Operations

1.  For each network segment in Input 1 `GV36`, use Input 3 to identify communication protocols

    1.  Identify and enumerate segments using only communication protocols on the authorized list (M2)
    2.  Identify and enumerate segments using communication protocols not on the authorized list (M3)

2.  For each communication protocol identified in Operation 1.1, check configuration standards `GV37`

    1.  Identify and enumerate segments using properly configured communication protocols (M4)
    2.  Identify and enumerate segments using improperly configured communication protocols (M5)

3.  For each network segment in Input 1 `GV36`, use Input 3 to identify network management protocols

    1.  Identify and enumerate segments using only network management protocols on the authorized list (M6)
    2.  Identify and enumerate segments using network management protocols not on the authorized list (M7)

4.  For each communication protocol identified in Operation 1.1, check configuration standards `GV37`

   1.  Identify and enumerate segments using properly configured network management protocols (M8)
   2.  Identify and enumerate segments using improperly configured network management protocols (M9)

### Measures

-   M1 = Count of `GV36`
-   M2 = Count of segments using authorized communication protocols
-   M3 = Count of segments using unauthorized communication protocols
-   M4 = Count of segments using properly configured authorized
    communication protocols
-   M5 = Count of segments using improperly configured authorized
    communication protocols
-   M6 = Count of segments using unauthorized network management
    protocols
-   M7 = Count of segments using unauthorized network management
    protocols
-   M8 = Count of segments using properly configured authorized network
    management protocols
-   M9 = Count of segments using improperly configured authorized
    network management protocols

### Metrics

#### Communication Protocol Coverage

| **Metric**      | The percentage of network segments using properly configured and authorized communication protocols |
|-----------------|------------------------------------------------------------------------------------------------------|
| **Calculation** | `M4 / M1`                                                                                            |


#### Network Management Protocol Coverage

| **Metric**      | The percentage of network segments using properly configured and authorized network management protocols|
|-----------------|---------------------------------------------------------------------------------------------------------|
| **Calculation** | `M8 / M1`                                                                                               |

