# 9.6: Block Unnecessary File Types

Block unnecessary file types attempting to enter the enterprises email
gateway.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standards

## Operations

1.  Use `GV1` to identify and enumerate assets configured as email
    gateways (M1)

2.  

    Using `GV3` check the attachment blocking configuration for every asset identified in Operation 1

    :   1.  Identify and enumerate email gateways properly configured to
            block unnecessary attachments (M2)
        2.  Identify and enumerate email gateways not properly
            configured to block unnecessary attachments (M3)

## Measures

-   M1 = Count of email gateways
-   M2 = Count of properly configured email gateways
-   M3 = Count of improperly configured email gateways

## Metrics

### Coverage

+-----------------+--------------------------------------------------------+
| **Metric**      | | The percentage of properly configured email gateways |
+-----------------+--------------------------------------------------------+
| **Calculation** | `M2 / M1`                                              |
+-----------------+--------------------------------------------------------+
