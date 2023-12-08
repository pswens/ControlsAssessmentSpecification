# 9.5: Implement DMARC

To lower the chance of spoofed or modified emails from valid domains,
implement DMARC policy and verification, starting with implementing the
Sender Policy Framework (SPF) and the DomainKeys Identified Mail (DKIM)
standards.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             2, 3

## Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory

## Inputs

1.  DMARC Policy
2.  TXT record published in DNS
3.  The Mail Transfer Agent used by the enterprise
4.  The Mail User Agent used by the enterprise

Assumptions \-\-\-\-\-\-\-\-\--#. The DMARC configuration policy
includes instructions to produce either Aggregate (rua) or Forensic
(ruf) reports. #. The enterprise has access to these reports either
daily (for Aggregate) or in real-time (for Forensic).

## Operations

1.  

    Check if enterprise has a DMARC policy

    :   1.  If the enterprise has a DMARC policy, M1 = 1
        2.  If the enterprise does not have a DMARC policy, M1 = 0

2.  

    Examine Input 2 for a value indicative of the use of DMARC

    :   1.  If a value for DMARC is identified, M2 = 1
        2.  If a value for DMARC is not identified, M2 = 0

3.  

    Examine Input 2 for a value indicative of the use of SPF

    :   1.  If a value for SPF is identified, M3 = 1
        2.  If a value for SPF is not identified, M3 = 0

4.  

    Examine Input 2 for a value indicative of the use of DKIM

    :   1.  If a value for DKIM is identified, M4 = 1
        2.  If a value for DKIM is not identified, M4 = 0

5.  

    Check if enterprise uses a Mail Transfer Agent

    :   1.  If the enterprise uses a Mail Transfer Agent, M5 = 1
        2.  It the enterprise does not use a Mail Transfer Agent, M5 = 1

6.  

    Check if enterprise uses a Mail User Agent

    :   1.  If the enterprise uses a Mail User Agent, M6 = 1
        2.  It the enterprise does not use a Mail User Agent, M6 = 1

## Measures

-   M1 = Output of Operation 1
-   M2 = Output of Operation 2
-   M3 = Output of Operation 3
-   M4 = Output of Operation 4
-   M5 = Output of Operation 5
-   M6 = Output of Operation 6

## Metrics

DMARC Usage \^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | Usage and configuration of DMARC/SPF/DKIM
    * - **Calculation**
      - :code:`(M1 + M2 + M3 + M4 + M5 + M6) / 6`
