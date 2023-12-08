# 18.8: Establish a Process to Accept and Address Reports of Software Vulnerabilities

Establish a process to accept and address reports of software
vulnerabilities, including providing a means for external entities to
contact your security group.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  N/A          N/A                 2, 3

## Dependencies

-   None

## Inputs

1.  Written process for accepting and addressing software
    vulnerabilities

## Operations

1.  Determine whether a written process for accepting and addressing
    software vulnerabilities exists (M1).

2.  

    Manually review the written process for accepting and addressing software vulnerabilities (Input 1).

    :   1.  Identify whether the document provides a means for external
            entities to contact your security group (M2)
        2.  Identify whether the document adequately describes the
            process for accepting reports of software vulnerabilities
            (M3)
        3.  Identify whether the document adequately describes the
            process for addressing those reports (M4)

## Measures

-   M1 = Boolean value indicating whether a written process for
    accepting and addressing software vulnerabilities exists; 1 if it
    exists, 0 if it does not
-   M2 = Boolean value indicating whether the document provides a means
    for external entities to contact your security group; 1 if the
    document provides this info, 0 if it does not
-   M3 = Boolean value indicating whether the document adequately
    describes the process for accepting reports of software
    vulnerabilities; 1 if the document adequately describes this
    process, 0 if it does not
-   M4 = Boolean value indicating whether the document adequately
    describes the process for addressing reports of software
    vulnerabilities; 1 if the document adequately describes this
    process, 0 if it does not

## Metrics

### Process Completeness

+-----------------+---------------------------------------------------+
| **Metric**      | | Does the written process for accepting and      |
|                 |   addressing reports of software                  |
|                 | | vulnerabilities exist and is it complete?       |
+-----------------+---------------------------------------------------+
| **Calculation** | `M1 AND M2 AND M3 AND M4`                         |
+-----------------+---------------------------------------------------+
