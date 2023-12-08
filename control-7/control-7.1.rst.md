# 7.1: Establish and Maintain a Vulnerability Management Process

Establish and maintain a documented vulnerability management process for
enterprise assets. Review and update documentation annually, or when
significant enterprise changes occur that could impact this Safeguard.

  Asset Type     Security Function   Implementation Groups
  -------------- ------------------- -----------------------
  Applications   Protect             1, 2, 3

## Dependencies

-   None

## Inputs

1.  Enterprise vulnerability management process
2.  Date of last update to the vulnerability management process

## Operations

1.  

    Determine wether the enterprise maintains a vulnerability management process

    :   1.  If the process exists, M1 = 1
        2.  If the process does not exist, M1 = 0

2.  Compare the date from Input 1 to the curren date and enumerate
    timeframe in months (M2)

## Measures

-   M1 = Output of Operation 1
-   M2 = Timeframe since last update to vulnerability management process

## Metrics

If M1 is 0, this safeguard receives a failing score. The other metrics
don\'t apply. If M2 is greater than twelve, this safeguard receives a
failing score. The other metrics don\'t apply.
