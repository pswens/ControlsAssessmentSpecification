16.7: Use Standard Hardening Configuration Templates for Application
Infrastructure =========================================================
Use standard, industry-recommended hardening configuration templates for
application infrastructure components. This includes underlying servers,
databases, and web servers, and applies to cloud containers, Platform as
a Service (PaaS) components, and SaaS components. Do not allow in-house
developed software to weaken configuration hardening.

  Asset Type     Security Function   Implementation Groups
  -------------- ------------------- -----------------------
  Applications   Protect             2, 3

# Dependencies

-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process
-   Safeguard 4.2: Establish and Maintain a Secure Configuration Process
    for Network Infrastructure

# Inputs

1.  `GV1`: Enterprise Asset Inventory
2.  `GV37`: Network infrastructure configuration standards

# Operations

1.  Use Input 1 `GV1` to identify and enumerate application
    infrastructure components `GV50` (M1)

2.  

    For each infastructure component identified in Operation 1, check configurations using Input 2 `GV37` and determine if they meet industry recommended hardening configuraion standards

    :   1.  Identify and enumerate infrastructure components that meet
            industry standards (M2)
        2.  Identify and enumerate infrastructure components that do not
            meet industry standards (M3)

# Measures

-   M1 = Count of application infrastructure components
-   M2 = Count of components that meet industry standards
-   M3 = Count of components that do not meet industry standards

# Metrics

## Compliance

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of application infrastructure    |
|                 |   components that meet                            |
|                 | | industry configuration standards                |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / M1`                                         |
+-----------------+---------------------------------------------------+
