9.7: Deploy and Maintain Email Server Anti-Malware Protections
========================================================= Deploy and
maintain email server anti-malware protections, such as attachment
scanning and/or sandboxing.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             3

# Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

# Inputs

1.  `GV1`: Enterprise asset inventory
2.  `GV3`: Configuration standard

# Operations

1.  Use `GV1` to identify and enumerate all email servers within the
    enterprise (M1)

2.  

    For each email server identified in Operation 1, use `GV3` to check if native or external anti-malware protections are configured

    :   1.  Identify and enumerate email servers with configured
            anti-malware protection (M2)
        2.  Identify and enumerate email servers without configured
            anti-malware protection (M3)

# Measures

-   M1 = Count of email servers
-   M2 = Count of properly configured email servers
-   M3 = Count of improperly configured email servers

# Metrics

## Coverage

+-----------------+-------------------------------------------------------+
| **Metric**      | | The percentage of properly configured email servers |
+-----------------+-------------------------------------------------------+
| **Calculation** | `M2 / M1`                                             |
+-----------------+-------------------------------------------------------+
