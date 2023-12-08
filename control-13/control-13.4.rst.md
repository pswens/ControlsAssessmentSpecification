# 13.4: Perform Traffic Filtering Between Network Segments

Perform traffic filtering between network segments, where appropriate.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Network      Protect             2, 3

## Dependencies

-   None

## Inputs

1.  `GV36`: Segments within the enterprise network
2.  `GV35`: Assets that are part of the network infrastructure
3.  `GV37`: Network infrastructure configuration standards

## Operations

1.  Use Input 1 `GV36` to identify and enumerate network segments that
    require communication with other network segments (M1)

2.  For each network segment identified in Operation 1, use Input 2
    `GV35` to identify network infrastructure assets responsible for
    traffic filtering

3.  

    For each network infrastructure asset identified in Operation 1, check configurations using Input 3 `GV37` to determine whether each semgment is properly configured to filter traffic

    :   1.  Identify and enumerate network segments with properly
            configured filtering assets (M2)
        2.  Identify and enumerate network segments with improperly
            configured filtering assets (M3)

## Measures

-   M1 = Count of network segments that communicate with other network
    segments
-   M2 = Count of network segments with properly configured filtering
    assets
-   M3 = Count of network segments wih improperly configured filtering
    assets

## Metrics

### Coverage

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of network segments properly     |
|                 |   configured to                                   |
|                 | | filter traffic between segments                 |
+-----------------+---------------------------------------------------+
| **Calculation** | `M2 / M1`                                         |
+-----------------+---------------------------------------------------+
