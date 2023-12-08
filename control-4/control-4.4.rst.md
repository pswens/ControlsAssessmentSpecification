# 4.4: Implement and Manage a Firewall on Servers

Implement and manage a firewall on servers, where supported. Example
implementations include a virtual firewall, operating system firewall,
or a third-party firewall agent.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Devices      Protect             1, 2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV5`: Authorized software inventory
3.  `GV3`: Configuration standard

## Operations

1.  Identify and enumerate servers capable of hosting a firewall using
    `GV1` (M1)

2.  Identify and enumerate applications capable of hosting a firewall
    using `GV5` (M2)

3.  

    Using configuration standards to check if firewalls are properly configured

    :   1.  Enumerate servers from Operation 1 with properly configured
            firewalls (M3)
        2.  Enumerate servers from Operation 1 with improperly
            configured firewalls (M4)
        3.  Enumerate applications from Operation 2 with properly
            configured firewalls (M3)
        4.  Enumerate application from Operation 2 with improperly
            configured firewalls (M4)

## Measures

-   M1 = Count of servers enterprise assets capable of hosting a
    firewall
-   M2 = Count of applications software capable of hosting a firewall
-   M3 = Count of servers with properly configured firewalls
-   M4 = Count of servers with improperly configured firewalls
-   M5 = Count of applications with properly configured firewalls
-   M6 = Count of applications with improperly configured firewalls

## Metrics

Implementation of firewalls
\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of properly configured firewalls within the enterprise
    * - **Calculation**
      - :code:`(M3 + M5) / (M1 + M2)`
