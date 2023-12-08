# 6.8: Define and Maintain Role-Based Access Control

Define and maintain role-based access control, through determining and
documenting the access rights necessary for each role within the
enterprise to successfully carry out its assigned duties. Perform access
control reviews of enterprise assets to validate that all privileges are
authorized, on a recurring schedule at a minimum annually, or more
frequently.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Protect             3

## Dependencies

-   Safeguard 5.1: Establish and Maintain an Inventory of Accounts

## Inputs

1.  Enterprise documented process for assigning role-based access
    control
2.  `GV22`: Inventory of accounts
3.  Date of last validation of role-based access control

## Operations

1.  

    Determine whether the enterprise has a process for assigning role-based access control

    :   1.  If the process exists, M1 = 1
        2.  If the process does not exist, M1 = 1

2.  

    Use `GV22` and check if each account is assigned a role or group as outlined by the role-based access control process

    :   1.  Identify and enumerate accounts that are assigned a role or
            group (M3)
        2.  Identify and enumerate accounts that are not assigned a role
            or group (M4)

3.  Compare the date in Input 3 to the current date and capture
    timeframe in months (M5)

## Measures

-   M1 = Does a role-based access control process exist as defined by
    the Output of Operation 1
-   M2 = Count of `GV22`
-   M3 = Count of accounts found in the inventory with assigned role or
    group
-   M4 = Count of accounts found in the inventory not assigned a role or
    group
-   M5 = Timeframe in months of last review of role-bases access control
    process

## Metrics

If M1 is 0, this safeguard receives a failing score. The other metrics
don\'t apply. If M5 is greater than twelve months, this safeguard is
measured at a 0 and receives a failing score. The other metrics don\'t
apply.

### Coverage

+-----------------+-------------------------------+------------------+
| **Metric**      | | The percentage of account   | | role or group. |
|                 |   inventory with a properly   |                  |
|                 |   assigned                    |                  |
+-----------------+-------------------------------+------------------+
| **Calculation** | `M3 / M2`                     |                  |
+-----------------+-------------------------------+------------------+
