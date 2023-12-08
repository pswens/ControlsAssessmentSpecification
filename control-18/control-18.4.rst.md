# 18.4: Validate Security Measures

Validate security measures after each penetration test. If deemed
necessary, modify rulesets and capabilities to detect the techniques
used during testing.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             3

## Dependencies

-   Safeguard 18.1: Establish and Maintain a Penetration Testing Program

## Inputs

1.  `GV53`: Penetration Testing Program Documentation
2.  `GV54`: Most Recent External Penetration Report
3.  `GV55`: Most Recent Internal Penetration Report

## Operations

1.  

    Check Input 1 `GV53` to determine if it incluces an enterprise process for validating security measures after a penetration test

    :   1.  If the process exists, M1 = 1
        2.  If the process does not exist, M1 = 0

2.  Using the findings from both Input 2 `GV54` an Input 3 `GV55`, as
    applicable, identify and enumerate security measures that required
    modification (M2)

3.  

    For each security measure identified in Operation 2, check if modifications have been made

    :   1.  Identify and enumerate security measures that have been
            modified per the enterprise\'s defined process (M3)
        2.  Identify and enumerate security measures not yet modified
            per the enterprise\'s defined process (M4)

## Measures

-   M1 = Output of Operation 1
-   M2 = Count of security measures requiring modification
-   M3 = Count of security measures requiring modification that are
    properly addressed
-   M4 = Count of security measures requiring modification that are not
    yet addressed

## Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.

Compliance \^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of security measures requiring modification that have
        | been properly addressed
    * - **Calculation**
      - :code:`M3 / M2`
