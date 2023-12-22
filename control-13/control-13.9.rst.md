## 13.9: Deploy Port-Level Access Control

Deploy port-level access control. Port-level access control utilizes
802.1x, or similar network access control protocols, such as
certificates, and may incorporate user and/or device authentication.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Devices      | Protect             | 3                     |

### Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory

### Inputs

1.  `GV5`: Authorized Software Inventory
2.  `GV38`: AAA services within the enterprise
3.  `GV41`: List of CMDB servers
4.  `GV35`: Assets that are part of the network infrastructure
5.  `GV37`: Network infrastructure configuration standards

### Operations

1.  If the enterprise uses an 802.1x network design to control network
access:

    1. Use Input 1 `GV5` to identify and enumerate 802.1x authenticators

2.  For each authenticator identified in Operation 1, use Input 5 `GV37` to check configurations

    1.  Identify and enumerate properly configured authenticators (M2)
    2.  Identify and enumerate improperly configured authenticators (M3)

3.  Use Input 2 `GV38` to identify 802.1x authentication servers (M4)

4.  For each authentication server identified in Operation 3, use Input 5 `` GV37`to check configurations to ensure a connection to at least one CMDB server from Input 3:code:`GV41 ``

    1.  Identify and enumerate properly configured authentication servers (M5)
    2.  Identify and enumerate improperly configured authentication servers (M6)

5.  If the enterprise does not use 802.1x network design to control network
access:

    1. For each asset in Input 4 `GV35`, use Input 5 `GV37` to check client authentication certificate configuration

        1.  Identify and enumerate properly configured assets (M8)
        2.  Identify and enumerate improperly configured assets (M9)

### Measures

-   M1 = Count of 802.1x authenticators
-   M2 = Count of 802.1x properly configured authenticators
-   M3 = Count of 802.1x improperly configured authenticators
-   M4 = Count of 802.1x authentication servers
-   M5 = Count of 802.1x properly configured authentication servers
-   M6 = Count of 802.1x improperly configured authentication servers
-   M7 = Count of Input 4 `GV35`
-   M8 = Count of assets properly configured for client authentication
    certificates
-   M9 = Count of assets improperly configured for client authentication
    certificates

### Metrics

If the enterprise uses an 802.1x network design to control network
access:

#### Authenticator Coverage 

| **Metric**      | The percentage of properly configured authenticators |
|-----------------|----------------------------------------------------|
| **Calculation** | `M2 / M1`                                          |

#### Authentication Server Coverage

| **Metric**      | The percentage of properly configured authentication servers |
|-----------------|----------------------------------------------------------|
| **Calculation** | `M5 / M4`                                                |


If the enterprise does not use 802.1x network design to control network
access:

#### Client Authentication Certificate Coverage

| **Metric**      | The percentage of assets properly configured for authentication certificate coverage |
|-----------------|-----------------------------------------------------------------------------------------|
| **Calculation** | `M8 / M7`                                                                               |

