# 5.3: Disable Dormant Accounts

Delete or disable any dormant accounts after a period of 45 days of
inactivity, where supported

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Respond             1, 2, 3

## Dependencies

-   Safeguard 5.1: Establish and Maintain an Inventory of Accounts

## Inputs

1.  `GV22`: Inventory of accounts
2.  Enterprise defined policy for dormant threshold

Assumptions \-\-\-\-\-\-\-\-\--#. The list of accounts for the
enterprise includes OS-level, database, internal and external
application accounts. #. A query interface is assumed to enable
collection of a "last activity" timestamp, such as last logon, as well
as a status indicating if the account is enabled or disabled.

## Operations

1.  Review Input 2 and note the dormant threshold in terms of days (M2)

2.  

    For each account in `GV22`, query the interface and collect

    :   1.  The date of last activity for each account
        2.  Whether the account is disabled or not

3.  

    Using the output of Operation 2.1 and Input 2

    :   1.  Identify and enumerate accounts that have exceeded the
            dormant threshold (M3)
        2.  Identify and enumerate accounts that are still within the
            dormant threshold (M4)

4.  

    Use the output of Operation 2.2 and 3.1 (M3)

    :   1.  Identify and enumerate accounts that are disabled (M5)
        2.  Identify and enumerate accounts that are still enabled (M6)

## Measures

-   M1 = Count of accounts in `GV22`
-   M2 = Timeframe of dormant threshold in days
-   M3 = Count of dormant accounts
-   M4 = Count of active accounts
-   M5 = Count of dormant accounts that have been disabled
-   M6 = Count of dormant accounts still enabled

## Metrics

### Dormant Accounts

+-----------------+-------------------------------+------------------+
| **Metric**      | | The percentage of dormant   | | the inventory. |
|                 |   accounts still included in  |                  |
+-----------------+-------------------------------+------------------+
| **Calculation** | `M6 / M1`                     |                  |
+-----------------+-------------------------------+------------------+

Enabled Dormant Accounts \^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^\^ ..
list-table:

    * - **Metric**
      - | The percentage of dormant accounts still enabled
    * - **Calculation**
      - :code:`M6 / M3`
