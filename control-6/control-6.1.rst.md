# 6.1: Establish an Access Granting Process

Establish and follow a process, preferably automated, for granting
access to enterprise assets upon new hire, rights grant, or role change
of a user.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             1, 2, 3

## Dependencies

-   None

## Inputs

1.  Enterprise process for granting access to enterprise assets

## Operations

1.  

    Check to see if Input 1 exists

    :   1.  If the enterprise has an access granting process, M1 = 1
        2.  If the enterprise does not have an access granting process,
            M1 = 0

2.  

    Using Input 1, check to see if the process, includes at a minimum, a way to grant access upon new hire, rights grat, and role change of a user.

    :   1.  For each element that is include, assign a value of 1. Sum
            the value of the elemnts included. (M2)

## Measures

-   M1 = Output of Operation 1
-   M2 = Count of elements included in the access granting process

## Metrics

If M1 is 0, the safeguard receives a failing score. The other metric
don\'t apply.

### Completeness of Process

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of elements included in the      |
|                 |   access granting process                         |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / 3`                                          |
+-----------------+---------------------------------------------------+
