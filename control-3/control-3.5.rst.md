# 3.5: Securely Dispose of Data

Securely dispose of data as outlined in the enterprise's data management
process. Ensure the disposal process and method are commensurate with
the data sensitivity.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Protect             1, 2, 3

## Dependencies

-   Safeguard 3.1: Establish and Maintain a Data Management Process
-   Safeguard 3.2: Establish and Maintain a Data Inventory

## Inputs

1.  `GV16`: Data disposal requirement portion of data management process
2.  `GV11`: Portion of data management process addressing data
    sensitivity
3.  `GV17`: Count of Sensitive data types
4.  `GV12`: Sensitive Data Inventory

## Operations

1.  

    For each sensitive data type covered in `GV17`

    :   1.  Identify and enumerate each type has a disposal method and
            process as defined by `GV16` (M2)
        2.  Identify and enumerate each type that does not have a
            disposal method and process as defined by `GV16`(M3)

2.  

    For each item in `` GV12`determine wether they data complies with the disposal requirements outlined in :code:`GV17 ``

    :   1.  Enumerate data that does not comply with disposal
            requirements (M4)
        2.  Enumerate data that complies with disposal requirements (M5)

## Measures

-   M1 = `GV17`
-   M2 = Count of sensitive data types with an outlined disposal method
-   M3 = Count of sensitive data types without an outlined disposal
    method
-   M4 = Count of data in inventory that does not comply with disposal
    requirement
-   M5 = Count of data in inventory that complies with disposal
    requirement
-   M6 = Count of items in `GV12`

## Metrics

-   If `GV16` is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.

### Completeness of disposal process

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of data sensitivity types that   |
|                 |   contain a disposal method and process           |
+-----------------+---------------------------------------------------+
| **Calculation** | | `M2 / M1`                                       |
+-----------------+---------------------------------------------------+

### Compliance to disposal process

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of compliance to the data        |
|                 |   disposal process                                |
+-----------------+---------------------------------------------------+
| **Calculation** | | `M5 / M6`                                       |
+-----------------+---------------------------------------------------+
