## 12.7: Ensure Remote Devices Utilize a VPN and are Connecting to an Enterprise's AAA Infrastructure

Require users to authenticate to enterprise-managed VPN and authentication services
prior to accessing enterprise resources on end-user devices.

| Asset Type   | Security Function   | Implementation Groups |
| ------------ | ------------------- | --------------------- |
| Devices      | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 12.5: Centralize Network Authentication, Authorization,
    and Auditing (AAA)

### Inputs

1.  `GV1`: Enterprise Asset Inventory
2.  `GV5`: Authorized Software Inventory
3.  `GV38`: AAA services within the enterprise
4.  `GV37`: Network infrastructure configuration standards

### Operations

1.  Use Input 1 `GV1` to identify and enumerate remote enterprise assets
    `GV39` (M1)

2.  Use Input 1 `GV1` and Input 2 `GV5` to identify and enumerate all
    VPN devices and software (M2)

3.  Use the output of Operation 2 and Input 4 `GV37` to check the configuration of the VPN

    1.  Identify and enumerate VPN devices and software properly configured to require authentication prior to granting access (M3)
    2.  Identify and enumerate VPN devices and software not properly configured to require authentication prior to granting access (M4)

4. For each asset identified in Operation 1, check if is covered by a VPN device or software identified in Operation 3.1

    1.  Identify and enumerate assets that are covered by a VPN (M5)
    2.  Identify and enumerate assets that are not covered by a VPN (M6)

5.  Use Input 3 `GV38` and Input 4 `GV37` to check configuration of AAA services

    1.  Identify and enumerate AAA services properly configured to require authentication prior to granting access (M7)
    2.  Identify and enumerate AAA services not properly configured to require authentication prior to granting access (M8)

6.  For each asset identified in Operation 1, check if it is covered by an AAA service identified in Operation 5.1

    1.  Identify and enumerate assets that are covered by an AAA service (M9)
    2.  Identify and enumerate assets that are not covered by an AAA service (M10)

7.  Compare the output of Operation 4.1 and 6.1

    1.  Identify and enumerate assets covered by both VPN and AAA (M1)

### Measures

-   M1 = Count of remote enterprise assets
-   M2 = Count of VPN devices and software
-   M3 = Count of properly configured VPN devices and software
-   M4 = Count of improperly configured VPN devices and software
-   M5 = Count of remote assets covered by a properly configured VPN
-   M6 = Count of remote assets not covered by a properly configured VPN
-   M7 = Count of properly configured AAA services
-   M8 = Count of improperly configured AAA services
-   M9 = Count of remote assets covered by a properly configured AAA
    service
-   M10 = Count of remote assets not covered by a properly configured
    AAA service
-   M11 = Count of remote assets covered by both VPN and AAA
-   M12 = Count of AAA services within the enterprise

### Metrics

#### VPN Compliance 

| **Metric**      | The percentage of properly configured VPN devices and software |
|-----------------|--------------------------------------------------------------|
| **Calculation** | `M3 / M2`                                                    |

#### AAA Compliance

| **Metric**      | The percentage of properly configured AAA services |
|-----------------|--------------------------------------------------|
| **Calculation** | `M7 / M12`                                       |

## Coverage

| **Metric**      | The percentage of remote assets using VPN and AAA |
|-----------------|--------------------------------------------------|
| **Calculation** | `M11 / M1`                                       |
