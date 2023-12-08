# 15.7: Securely Decommission Service Providers

Securely decommission service providers. Example considerations include
user and service account deactivation, termination of data flows, and
secure disposal of enterprise data within service provider systems

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Data         Protect             3

## Dependencies

-   Safeguard 15.1: Establish and Maintain an Inventory of Service
    Providers
-   Safeguard 15.2: Establish and Maintain a Service Provider Management
    Policy

## Inputs

1.  `GV44`: Service Provider Inventory List
2.  `GV45`: Service Provider Management Policy

## Operations

1.  

    Use Input 2 `GV45` to determine if the enterprise policy includes guidance for securely decommissioning service providers

    :   1.  If the monitoring guidance exist, M1 = 1
        2.  If the monitoring guidance does not exist, M1 = 0

2.  Use Input 1 `GV44` to identify and enumerate any service providers
    terminated over the last twelve months (M2)

3.  

    For each service provider identified in Operation 2, determine if the provider was decommissioned per the policy

    :   1.  Identify and enumerate service providers properly terminated
            (M3)
        2.  Identify and enumerate service providers improperly
            terminated (M4)

## Measures

-   M1 = Output of Operation 1
-   M2 = Count of service providers terminated over the last twelve
    months
-   M3 = Count of service providers properly terminated
-   M4 = Count of service providers improperly terminated

## Metrics

-   If M1 is a 0, this safeguard receives a failing score. The other
    metrics don\'t apply.

Compliance \^\^\^\^\^\^\^\^ .. list-table:

    * - **Metric**
      - | The percentage of service providers properly terminated
    * - **Calculation**
      - :code:`M3 / M2`
