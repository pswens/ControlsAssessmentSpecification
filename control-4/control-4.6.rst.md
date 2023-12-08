# 4.6: Securely Manage Enterprise Assets and Software

Securely manage enterprise assets and software. Example implementations
include managing configuration through
version-controlled-infrastructure-as-code and accessing administrative
interfaces over secure network protocols, such as Secure Shell (SSH) and
Hypertext Transfer Protocol Secure (HTTPS). Do not use insecure
management protocols, such as Telnet (Teletype Network) and HTTP, unless
operationally essential.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             1, 2, 3

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

1.  Using `GV5` identify and enumerate authorized management software
    (M1)

2.  Using `GV1` identify and enumerate assets capable of supporting
    management software (M2)

3.  Using the output of Operations 1 and 2, identify and enumerate
    assets with authorized management software installed (M3)

4.  

    Using configuration standards `GV3` to check if management software is configured properly

    :   1.  Enumerate assets from Operation 3 with properly configured
            management software (M4)
        2.  Enumerate assets from Operation 1 with improperly configured
            mangement software (M5)

## Measures

-   M1 = Count of authorized management software
-   M2 = Count of enterprise assets capable of supporting management
    software
-   M3 = Count of assets with authorized management software installed
-   M4 = Count of assets with properly configured management software
-   M5 = Count of assets with improperly configured management software

## Metrics

### Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of assets with properly          |
|                 |   configured authorized management software       |
+-----------------+---------------------------------------------------+
| **Calculation** | `M4 / M2`                                         |
+-----------------+---------------------------------------------------+
