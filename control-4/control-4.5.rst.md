# 4.5: Implement and Manage a Firewall on End-User Devices

Implement and manage a host-based firewall or port-filtering tool on
end-user devices, with a default-deny rule that drops all traffic except
those services and ports that are explicitly allowed.

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

1.  Identify and enumerate end-user devices capable of hosting a
    firewall or a deny rule using `GV1` (M1)

2.  

    Using configuration standards `GV3` to check if firewalls or deny rules are properly configured on end-user devices

    :   1.  Enumerate assets from Operation 1 with properly configured
            firewalls or a configured default deny rule (M3)
        2.  Enumerate assets from Operation 1 with improperly configured
            firewalls and lacking a configured default deny rule(M4)

## Measures

-   M1 = Count of end-user devices capable of hosting a firewall
-   M2 = Count of end-user devices with a properly configured firewall
    or default deny rule
-   M3 = Count of end-user devices with an improperly configured
    firewall and lacking a configured default deny rule

## Metrics

### Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of properly configured firewalls |
|                 |   or deny rule on end-user devices                |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / M1`                                         |
+-----------------+---------------------------------------------------+
