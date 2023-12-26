## 16.10: Apply Secure Design Principles in Application Architectures

Apply secure design principles in application architectures. Secure design principles
include the concept of least privilege and enforcing mediation to
validate every operation that the user makes, promoting the concept of
"never trusting user input." Examples include ensuring that explicit
error checking is performed and documented for all input, including for
size, data type, and acceptable ranges or formats. Secure design also
means minimizing the application infrastructure attack surface, such as
turning off unprotected ports and services, removing unnecessary
programs and files, and renaming or removing default accounts.

| Asset Type     | Security Function   | Implementation Groups |
| -------------- | ------------------- | --------------------- |
| Applications   | Protect             | 2, 3                  |

### Dependencies

-   Safeguard 16.1: Establish and Maintain a Secure Application
    Development Process

### Inputs

1.  `GV49`: Secure Application Development Process
2.  `GV50`: Application Infrastructure Components

### Operations

1.  Use Input 1 `GV49` to determine whether the process outlines a secure software framework that includes secure design principles

    1.  If the framework exists, M1 = 1
    2.  If the framework does not exist, M1 = 0

2.  For each application infrastructure component in Input 2 `GV50`, determine whether the secure design principles were applied per the framework

    1.  Identify and enumerate application infrastructure components where design principles are applied (M3)
    2.  Identify and enumerate application infrastructure components where design principles are not applied (M4)

### Measures

-   M1 = Output of Operation 1
-   M2 = Count of Input 2 `GV50`
-   M3 = Count of applications infrastructure components with design
    principles applied
-   M4 = Count of applications infrastructure components without design
    principles applied

### Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.

#### Compliance

| **Metric**      | The percentage of applications infrastructure components where design principles were applied |
|-----------------|---------------------------------------------------------------------------------------------|
| **Calculation** | `M3 / M2`                                                                                    |

