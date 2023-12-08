# 6.2: Establish an Access Revoking Process

Establish and follow a process, preferably automated, for revoking
access to enterprise assets, through disabling accounts immediately upon
termination, rights revocation, or role change of a user. Disabling
accounts, instead of deleting accounts, may be necessary to preserve
audit trails.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             1, 2, 3

## Dependencies

-   None

## Inputs

1.  Enterprise process for revoking access to enterprise assets

## Operations

1.  

    Check to see if Input 1 exists

    :   1.  If the enterprise has an access revoking process, M1 = 1
        2.  If the enterprise does not have an access revoking process,
            M1 = 0

2.  

    Using Input 1, check to see if the process, includes at a minimum, a way to revoke access upon termination, rights revocation, and role change of a user.

    :   1.  For each element that is include, assign a value of 1. Sum
            the value of the elemnts included. (M2)

## Measures

-   M1 = Output of Operation 1
-   M2 = Count of elements included in the access revoking process

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
