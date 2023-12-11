## 2.6: Allowlist Authorized Libraries

Use technical controls to ensure that only authorized software libraries,
such as specific .dll, .ocx, .so, etc. files, are allowed to load into a
system process. Block unauthorized libraries from loading into a system
process. Reassess bi-annually or more frequently.

| Asset Type    | Security Function | Implementation Groups |
| -------------- | ------------------ | ---------------------- |
| Applications   | Protect            | 2, 3                   |

### Dependencies

-   Safeguard 2.1: Establish and Maintain a Software Inventory
-   Safeguard 2.5: Allowlist Authorized Software
-   Safeguard 4.2: Establish and Maintain a Secure Configuration Process
    for Network Infrastructure

### Inputs

1.  `GV8`: Authorized allowlisting software
2.  The list of authorized software libraries
3.  `GV9`: Approved configuration (s) for allowlisting software
4.  Date of the last assessement of this safeguard

### Operations

1. For each item identified in `GV8, use the approved configurations from code: GV9` and authorized library list from Input 2:

    1. Identify and enumerate allowlisting software properly configured to allow process loading of authorized libraries (M2)
    2. Identify and enumerate allowlisting software improperly configured to allow process loading of authorized libraries (M3)


2.  Compare the date from Input 4 to the current date and note the timeframe in
    months (M4).

### Measures

-   M1 = Count :code:\`GV8
-   M2 = Count of properly configured allowlisting software
-   M3 = Count of improperly configured allowlisting software
-   M4 = Timeframe since the last assessment of this safeguard

### Metrics

-   If M4 is greater than six months, then this safeguard is measured at
    a 0 and receives a failing score. The other metrics don't apply.

#### Coverage

| **Metric**      | The percentage of appropriately configured allowlisting software instances within the enterprise. |
| :-------------- | :-------------------------------------------------------------------------------------------------- |
| **Calculation** | `M2 / M1`                                                                                        |

