2.1: Establish and Maintain a Software Inventory
============================================== Establish and maintain a
detailed inventory of all licensed software installed on enterprise
assets. The software inventory must document the title, publisher,
initial install/use date, and business purpose for each entry; where
appropriate, include the Uniform Resource Locator (URL), app store(s),
version(s), deployment mechanism, and decommission date. Review and
update the software inventory bi-annually, or more frequently.

  Asset Type     Security Function   Implementation Groups
  -------------- ------------------- -----------------------
  Applications   Identify            1, 2, 3

# Dependencies

-   None

# Inputs

1.  `GV5`: The authorized software inventory with detailed information
    including: timestamp indicating both last updated and last verified
    values, timestamp indicating installation date, operating system,
    software name, software version, software publisher, authorization
    status, business purpose, supported/unsupported. Where applicable,
    additionally include URL, app store(s), deployment mechanism, and
    decommission date.
2.  `GV6`: The date of the last update to the authorized software
    inventory.

# Operations

1.  

    Check `GV5` for completeness of detailed information.

    :   1.  Note items that have complete detailed information (M2).
        2.  Note items that having missing or incomplete information
            (M3).

2.  Compare the current date to `GV6` and note timeframe in months (M4).

# Measures

-   M1 = Count of `GV5`
-   M2 = Count of items in `GV5` with complete information
-   M3 = Count of items in `GV5` with incomplete or missing information
-   M4 = Timeframe in months since last update `GV6`

# Metrics

-   If M1 is not provided or available, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.
-   If M4 is greater than six months, then this safeguard is measured at
    a 0 and receives a failing score. The other metrics don\'t apply.

## Accuracy Score

+-----------------+---------------------------------------------------+
| **Metric**      | | What percentage of the current enterprise asset |
|                 |   inventory contains necessary detailed           |
|                 |   information?                                    |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / M1`                                         |
+-----------------+---------------------------------------------------+
