# 8.3: Ensure Adequate Audit Log Storage

Ensure that logging destinations maintain adequate storage to comply
with the enterprise's audit log management process.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             1, 2, 3

## Dependencies

-   Safeguard 1.1: Establish and Maintain Detailed Enterprise Asset
    Inventory

## Inputs

1.  `GV27`: Assets capable of supporting logging
2.  `GV26`: Enterprise\'s audit log management process

Assumptions \-\-\-\-\-\-\-\-\--#. It is assumed that if the an asset is
properly configured to meet the retention policy, that would include log
rotation, maximum storage size, etc.

## Operations

1.  For each asset in `GV27` collect the asset\'s logging configuration

2.  

    Compare the output of Operation 1 and the retention portion of `G26`

    :   1.  Identify and enumerate assets configured to comply with the
            retention portion of the process (M2)
        2.  Identify and enumerate assets not configured to comply with
            the retention portion of the process (M3)

## Measures

-   M1 = Count of `GV27` assets capable of supporting logging
-   M2 = Count of assets properly configured to meet retention
    requirements
-   M3 = Count of assets not properly configured to meet retention
    requirements

## Metrics

Logging Storage Coverage \^\^\^\^\^\^\^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of assets compliant with the organization's logging 
      - |  policy
    * - **Calculation**
      - :code:`M2 / M1`
