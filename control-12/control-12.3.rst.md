## 12.3: Securely Manage Network Infrastructure

Securely manage network infrastructure. Example implementations include
version-controlled-infrastructure-as-code, and the use of a secure network
protocols, such as SSH and HTTPS.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Network      | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.2: Establish and Maintain a Secure Configuration Process
    for Network Infrastructure
-   Safeguard 12.4: Establish and Maintain Architecture Diagram(s)

### Inputs

1.  `GV36`: Segments within the enterprise network
2.  `GV35`: Assets that are part of the network infrastructure
3.  `GV37`: Network architecture configuration standards

### Operations

1.  For each asset in Input 2 `GV35`, use Input 3 `GV37` to check for the use of encrypted sessions

    1.  Identify and enumerate assets using encrypted sessions (M2)
    2.  Identify and enumerate assets not using encrypted sessions (M3)

2.  For each network segment in Input 1 `GV36`, check for the use of infrastructure-as-code

    1.  Identify and enumerate network segments that use infrastructure-as-code for the whole segment or partial (M5)
    2.  Identify and enumerate network segments that do not use infrastructure-as-code for any portion of the segment (M6)

3.  For each network segment identified in Operation 1, use Input 3 `GV37` to determine whether the infrastructure-as-code is managed using version control

    1.  Identify and enumerate network segments covered by version-controlled infrastructure-as-code (M7)
    2.  Identify and enumerate network segments covered by infrastructure-as-code is not managed through version control (M8)

### Measures

-   M1 = Count of `GV35` assets that are part of the network
    infrastructure
-   M2 = Count of network infrastructure assets using encrypted sessions
-   M3 = Count of network infrastructure assets not using encrypted
    sessions
-   M4 = Count of `GV36` segments within the enterprise network
-   M5 = Count of network segments using infrastructure-as-code
-   M6 = Count of network segments not using infrastructure-as-code
-   M7 = Count of network segments covered by version controlled
    infrastructure-as-code
-   M8 = Count of network segments covered by unmanaged
    infrastructure-as-code

### Metrics

#### Encrypted Session Coverage

| **Metric**      | The percentage of network infrastructure assets using encrypted sessions |
|-----------------|------------------------------------------------------------------------|
| **Calculation** | `M2 / M1`                                                        |

#### Infrastructure-As-Code Coverage

| **Metric**      | The percentage of network segments covered by version-controlled infrastructure-as-code |
|-----------------|---------------------------------------------------------------------------------------------|
| **Calculation** | `M7 / M4`                                                                             |
