# 3.2: Establish and Maintain a Data Inventory

Establish and maintain a data inventory, based on the enterprise's data
management process. Inventory sensitive data, at a minimum. Review and
update inventory annually, at a minimum, with a priority on sensitive
data.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Identify            1, 2, 3

## Dependencies

-   Sub-control 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory

## Inputs

1.  `GV11`: Portion of data management process addressing data
    sensitivity
2.  `GV12`: Data Inventory consisting of the data set of sensitive
    information for which the enterprise is responsible
3.  `GV1`: Enterprise asset inventory
4.  Date of last update to the sensitive data inventory

## Operations

1.  

    Use `GV11` to map Input 2 to sensitivity per the guidance in the data management process

    :   1.  Identify and enumerate items in the data set that have a
            mapping (M2)
        2.  Identify and enumerate items in the data set that do not
            have a mapping (M3)

2.  

    Use `GV1` and M2 from Operation 1 to map the data set to assets storing data

    :   1.  Identify and enumerate items that have complete and correct
            mapping to asset and sensitivity (M4)
        2.  Identify and enumerate items that have partial mapping to
            sensitivity (M5)

3.  

    Use: code:[GV1]{.title-ref} and M3 from Operation 2 to map the data set, without sensitivity mapping, to assets storing data

    :   1.  Identify and enumerate items that have partial mapping to
            assets (M6)
        2.  Identify and enumerate items that have no mapping at all
            (M7)

4.  Compare current date to Input 4 and capture timeframe in months (M8)

## Measures

-   M1 = `GV11`
-   M2 = Count of sensitive data addressed in `GV11`
-   M3 = Count of sensitive data not addressed in `GV11`
-   M4 = Count of data with complete sensitivity and asset storage
    inventory
-   M5 = Count of data with partial mapping to sensitivity
-   M6 = Count of data with partial mapping to assets
-   M7 = Count of data with no mapping to sensitivity or asset
-   M8 = Timeframe since last update to sensitive data inventory in
    months
-   M9 = Count of items in `GV12`

## Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M9 is greater than 12 months, this safeguard is scored at zero
    and receives a failing score. The other metrics don\'t apply.

### Completeness of sensitive data inventory

+-----------------+------------------------------------------------+
| **Metric**      | | Percentage of data with complete information |
+-----------------+------------------------------------------------+
| **Calculation** | `M4 / M9`                                      |
+-----------------+------------------------------------------------+

Partial completeness of sensitive data inventory \^\^\^\^\^\^\^\^ ..
list-table:

    * - **Metric**
      - | Percentage of data with partial inventory
    * - **Calculation**
      - :code:`(M5 + M6) / M9`
