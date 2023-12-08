# 4.9: Configure Trusted DNS Servers on Enterprise Assets

Configure trusted DNS servers on enterprise assets. Example
implementations include: configuring assets to use enterprise-controlled
DNS servers and/or reputable externally accessible DNS servers.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Devices      Protect             2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standard

## Operations

1.  Use `GV1` to identify and enumerate authorizsed DNS servers (M1)

2.  Use `GV1` to identify and enumerate assets configured for authorized
    DNS servers (M2)

3.  

    Use `GV3` to check configuration of DNS servers identified on assets in Operation 2

    :   1.  Identify and enumerate assets with DNS servers that are
            properly configured (M3)
        2.  Identify and enumerate assets with DNS servers that are
            improperly configured (M4)

## Measures

-   M1 = Count of authorized DNS servers
-   M2 = Count of enterprise assets configured for DNS servers
-   M3 = Count of assets with properly configured DNS servers
-   M4 = Count of assets with improperly configured DNS servers

## Metrics

### Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of assets with properlyn         |
|                 |   configured DNS servers                          |
+-----------------+---------------------------------------------------+
| **Calculation** | `M3 / M2`                                         |
+-----------------+---------------------------------------------------+
