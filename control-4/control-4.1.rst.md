4.1: Establish and Maintain a Secure Configuration Process
========================================================= Establish and
maintain a secure configuration process for enterprise assets (end-user
devices, including portable and mobile, non-computing/IoT devices, and
servers) and software (operating systems and applications). Review and
update documentation annually, or when significant enterprise changes
occur that could impact this Safeguard.

  Asset Type     Security Function   Implementation Groups
  -------------- ------------------- -----------------------
  Applications   Protect             1, 2, 3

# Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory

# Inputs

1.  `GV2`: Authorized software inventory
2.  `GV1`: Enterprise asset inventory
3.  `GV3`: Configuration Standard: this should include any enterprise
    approved deviations from industry standard baselines such as CIS
    benchmarks, DISA Security Technical Implementation Guides (STIGs),
    or U.S. government configuration baselines (USGCB).
4.  Date of last review and updat of configuration standard

# Operations

1.  

    Identify whether Input 2 exists

    :   1.  If it exists M1 = 1
        2.  If it does not exist M1 = 0

2.  Identify and enumerate end-user devices, including portable and
    mobile, non-computing/IoT devices, and servers in `GV1` (M2)

3.  Using the output of Operation 2 (M2), identify and enumerate the
    software installed on the assets using `GV2` (M3)

4.  

    For each software identified in Operation 3 (M3)

    :   1.  Enumerate software that is listed in the configuration
            standard `GV3`(M4)
        2.  Enumerate software that is not listed in the configuration
            standard `GV3`(M5)

5.  Compare current date to date provided in Input 4. Note the timeframe
    in months (M6)

# Measures

-   M1 = Output of Operation 1
-   M2 = Count of applicable enterprise assets
-   M3 = Count of software insalled on applicable enterprise assets
-   M4 = Count of software that is listed in the configuration standard
-   M5 = Count of software that is not listed in the configuration
    standard
-   M6 = Timeframe since last review and update in months

# Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M6 is greater than twelve, this safeguard is measured at a 0 and
    receives a failing score. The other metrics don\'t apply.

## Standard Configuration Coverage

+-----------------+------------------------------+-------------------+
| **Metric**      | | The perecentage of         | | and maintained. |
|                 |   authorized software with   |                   |
|                 |   secure configuration       |                   |
|                 |   standards documented       |                   |
+-----------------+------------------------------+-------------------+
| **Calculation** | `M4 / M3`                    |                   |
+-----------------+------------------------------+-------------------+
