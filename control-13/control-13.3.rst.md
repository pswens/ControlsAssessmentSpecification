# 13.3: Deploy a Network Intrusion Detection Solution

Deploy a network intrusion detection solution on enterprise assets,
where appropriate. Example implementations include the use of a Network
Intrusion Detection System (NIDS) or equivalent cloud service provider
(CSP) service.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Detect              2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 12.4: Establish and Maintain Architecture Diagram(s)

## Inputs

1.  `GV35`: Assets that are part of the network infrastructure
2.  `GV4`: Enterprise Network Architecture Documentation

## Operations

1.  Use Input 1 `GV35` to identify the network intrusion detection
    solutions for the enterprise

2.  Use Input 2 `GV4` to identify and enumerate network boundaries (M1)

3.  

    For each network boundary identified in Operation 2, determine whether it is covered by at least one network intrusion detection solution

    :   1.  Identify and enumerate boundaries covered by at least one
            network intrusion detection solution (M2)
        2.  Identify and enumerate boundaries not covered by at least
            one network intrusion detection solution (M3)

## Measures

-   M1 = Count of network boundaries
-   M2 = Count of network boundaries covered by a network intrusion
    detection solution
-   M3 = Count of network boundaries not covered by a network intrusion
    detection solution

## Metrics

### Coverage

+-----------------+------------------------+-----------------------+
| **Metric**      | | The percentage of    | | detection solutions |
|                 |   network boundaries   |                       |
|                 |   covered by network   |                       |
|                 |   intrusion            |                       |
+-----------------+------------------------+-----------------------+
| **Calculation** | `M2 / M1`              |                       |
+-----------------+------------------------+-----------------------+
