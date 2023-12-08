8.1: Establish and Maintain an Audit Log Management Process
========================================================= Establish and
maintain an audit log management process that defines the enterprise's
logging requirements. At a minimum, address the collection, review, and
retention of audit logs for enterprise assets. Review and update
documentation annually, or when significant enterprise changes occur
that could impact this Safeguard.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             1, 2, 3

# Dependencies

-   None

# Inputs

1.  `GV26`: Enterprise\'s audit log management process
2.  Date of last review of the audit log management process

# Operations

1.  

    Check if :code:\`GV26\`the audit log management process exists

    :   1.  If it exists, M1 = 1
        2.  If it does not exist, M1 = 0

2.  

    Review `GV26` for elements of the process, at a minimum, address the collection, review, and retention of audit logs for enterprise assets.

    :   1.  For each element that exists, assign a value of 1. Sum the
            values of existing elements. (M2)

3.  Compare the date from Input 2 and the current date. Capture the
    timeframe in terms of months. (M3)

# Measures

-   M1 = Output of Operation 1
-   M2 = Count of elements included in the audit log management process
-   M3 = Timeframe since last review of the autid log management process

# Metrics

If M1 is 0, this safeguard receives a failing a score. The other metrics
don\'t apply. If M3 is greater than twelve, this safeguard is measured
at a 0 and receives a failing score. THe other metrics don\'t apply.

## Completeness

+-----------------+------------------------+-----------------------+
| **Metric**      | | The percentage of    | | management process. |
|                 |   elements included in |                       |
|                 |   the audit log        |                       |
+-----------------+------------------------+-----------------------+
| **Calculation** | `M2 / 3`               |                       |
+-----------------+------------------------+-----------------------+
