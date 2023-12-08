# 2.7: Allowlist Authorized Scripts

Use technical controls, such as digital signatures and version control,
to ensure that only authorized scripts, such as specific .ps1, .py, etc.
files, are allowed to execute. Block unauthorized scripts from
executing. Reassess bi-annually, or more frequently.

  Asset Type     Security Function   Implementation Groups
  -------------- ------------------- -----------------------
  Applications   Protect             3

## Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 4.1: Establish and Maintain a Secure Configuration Process

## Inputs

1.  `GV5`: Authorized allowlisting software
2.  The list of authorized scripts
3.  `GV3`: Approved configuration Standards
4.  Date of last assessement of this safeguard

## Operations

1.  Use `GV5` to identify and enumerate all enterprise authorized
    software capable of executing scripts, including allowlisting
    software, email client applications, and web client applications
    (M1)

2.  Use `GV3` to identify approved configurations for all software
    identified in Operation 1

3.  

    For each item in identified in Operation 1, use the approved configurations from Operation 2

    :   1.  Identify and enumerate software properly configured to allow
            execution of authorized and signed scripts from Input 2 (M2)
        2.  Identify and enumerate software improperly configured to
            allow execution of authorized and signed scripts from Input
            2(M3)

4.  Compare the date from Input 4 to current date and note timeframe in
    months (M4).

## Measures

-   M1 = Count of authorized software capable of executing scripts
-   M2 = Count of properly configured software
-   M3 = Count of improperly configured software
-   M4 = Timeframe since last assessment of this safeguard

## Metrics

-   If M4 is greater than six months, then this safeguard is measured at
    a 0 and receives a failing score. The other metrics don't apply.

### Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of appropriately configured      |
|                 |   allowlisting software instances within the      |
|                 |   enterprise.                                     |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / M1`                                         |
+-----------------+---------------------------------------------------+
