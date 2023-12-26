## 16.13: Conduct Application Penetration Testing

Conduct application penetration testing. For critical applications,
authenticated penetration testing is better suited to finding business
logic vulnerabilities than code scanning and automated security
testing. Penetration testing relies on the skill of the tester to
manually manipulate an application as an authenticated and
unauthenticated user. 

  Asset Type     Security Function   Implementation Groups
  -------------- ------------------- -----------------------
  Applications   Protect             3

### Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory

### Inputs

1.  `GV5`: Authorized Software Inventory
2.  Application Penetration Process for enterprise

### Operations

1. Determine whether Input 2 exists for the enterprise

    1.  If the process exists, M1 = 1
    2.  If the process does not exist, M1 = 0

2.  Use Input 1 `GV5` to identify and enumerate all applications within the enterprise (M2)

3.  For each application identified in Operation 2, determine whether an unauthenticated penetration test has been conducted per the process outlined in Input 2

    1.  Identify and enumerate applications that have been tested (M3)
    2.  Identify and enumerate applications that have not been tested (M4)

4.  Use the output of Operation 2 to identify and enumerate critical applications within the list of applications (M5)

5.  For each application identified in Operation 4, determine whether an authenticated penetration test has been conducted per the process outlined in Input 2

    1.  Identify and enumerate applications that have been tested (M6)
    2.  Identify and enumerate applications that have not been tested (M7)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of applications within the enterprise
-   M3 = Count of applications that have undergone unauthenticated
    penetration testing per enterprise\'s process
-   M4 = Count of applications that have not undergone unauthenticated
    penetration testing per enterprise\'s process
-   M5 = Count of critical applications
-   M6 = Count of critical applications that have undergone
    authenticated penetration testing per enterprise\'s process
-   M7 = Count of critical applications that have not undergone
    authenticated penetration testing per enterprise\'s process

### Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.

#### Unauthenticated Penetration Testing Coverage

| **Metric**      | The percentage of applications that underwent unauthenticated penetration testing per enterprise's process |
|-----------------|-----------------------------------------------------------------------------------------------------------|
| **Calculation** | `M3 / M2`                                                                                         |


#### Authenticated Penetration Testing Coverage

| **Metric**      | The percentage of critical applications that underwent authenticated penetration testing per enterprise's process |
|-----------------|-----------------------------------------------------------------------------------------------------------------|
| **Calculation** | `M6 / M5`                                                                                               |

