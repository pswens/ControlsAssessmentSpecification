# 7.2: Establish and Maintain a Remediation Process

Establish and maintain a risk-based remediation strategy documented in a
remediation process, with monthly, or more frequent, reviews.

  Asset Type     Security Function   Implementation Groups
  -------------- ------------------- -----------------------
  Applications   Respond             1, 2, 3

## Dependencies

-   None

## Inputs

1.  Enterprise remediation strategy process
2.  Date of last review of the process
3.  `GV18`: Enterprise assets storing, processing, and transmitting
    sensitive data

## Operations

1.  

    Determine whether the enterprise maintains a documented remediation process

    :   1.  If the process exists, M1 = 1
        2.  If the process does not exist, M1 = 0

2.  

    Check the documented remediation process to identify whether it includes a risk based process based on the following elements: Sensitive assets `GV18` and criticality of vulnerability

    :   1.  Each element, if included, gets a value of 1. Sum all
            elements (M2)

3.  Compare the date from Input 2 and current date. Enumerate the
    timeframe in terms of days (M3)

## Measures

-   M1 = Output of Operation 1
-   M2 = Sum of elements included in the remediation process
-   M3 = Timeframe since last review of process in days

## Metrics

If M1 is 0, the safeguard receives a failing score. The other metrics
don\'t apply. If M3 is greater than thirty, the safeguard receives a
failing score. The other metrics don\'t apply.

### Completenes

+-----------------+------------------------------------------------------+
| **Metric**      | | The percentage of elements included in the process |
+-----------------+------------------------------------------------------+
| **Calculation** | `M2 / 2`                                             |
+-----------------+------------------------------------------------------+
