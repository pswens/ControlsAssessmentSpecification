# 17.4: Establish and Maintain an Incident Response Process

Establish and maintain an incident response process that addresses roles
and responsibilities, compliance requirements, and a communication plan.
Review annually, or when significant enterprise changes occur that could
impact this Safeguard.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  N/A          Respond             2, 3

## Dependencies

-   None

## Inputs

1.  `GV51`: Enterprise Incident Response Documentation
2.  Date of last update or review of the documentation

## Operations

1.  

    Determine whether the enterprise documents an incident response process: `GV52` by reviewing Input 1 `GV51`. Input 1 can be an incident response plan or other documentation.

    :   1.  If documentation for an incident response process exists, M1
            = 1
        2.  If documentation for an incident response process does not
            exist, M1 = 0

2.  

    Determine whether the documentation, at a minimum, outlines the following components: roles and responsibilities, compliance requirements, and a communication plan

    :   1.  For each component included, assign a value of 1. Sum the
            values. (M2)

3.  Compare Input 2 to current date and capture timeframe in months (M3)

## Measures

-   M1 = Output of Operation 1
-   M2 = Count of components included for incident response process
    documentation
-   M3 = Timeframe since last update or review of documentation in
    months

## Metrics

-   If M1 is 0, this safeguard receives a failing score. The other
    metrics don\'t apply.
-   If M3 is greater than twelve months, then this safeguard is measured
    at a 0 and receives a failing score. The other metrics don\'t apply.

Completeness \^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of components included in documentation for 
        | designated incident handling personnel 
    * - **Calculation**
      - :code:`M2 / 3`
