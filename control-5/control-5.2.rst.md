# 5.2: Use Unique Passwords

Use unique passwords for all enterprise assets. Best practice
implementation includes, at a minimum, an 8-character password for
accounts using MFA and a 14-character password for accounts not using
MFA.

  Asset Type   Security Function   Implementation Groups
  ------------ ------------------- -----------------------
  Users        Protect             1, 2, 3

## Dependencies

-   None

## Inputs

1.  `GV20`: Unique password policy for the enterprise

## Operations

1.  

    Check if the enterprise has a unique password policy

    :   1.  If policy is available M1 = 1
        2.  Otherwise M1 = 0

2.  

    Review the policy and determine whether it includes password guidance for accounts without MFA

    :   1.  

            If guidance is included M2 = 1

            :   1.  

                    Does guidance, at a minimum, require a fourteen character password

                    :   1.  If password guidance is fourteen characters
                            or longer M3 = 1
                        2.  Otherwise M3 = 0

        2.  Otherwise M2 = 0

3.  

    Review the policy and determine whether it includes password guidance for accounts with MFA

    :   1.  

            If guidance is included M4 = 1

            :   

                \# Does guidance, at a minimu, require an eight character password

                :   1.  If password guidance is eight characters or
                        longer M5 = 1
                    2.  Otherwise M5 = 0

        2.  Otherwise M3 = 0

## Measures

-   M1 = Does a password policy exist
-   M2 = Does guidance exist for accounts without MFA
-   M3 = Does guidance for accounts without MFA meet minimum guidance
-   M4 = Does guidance exist for accounts with MFA
-   M5 = Does guidance for accounts with MFA meet minimum guidance

## Metrics

If M1 is 0, the safeguard recieves a failing score. Other metrics don\'t
apply

Completeness of Password Policy \^\^\^\^\^\^\^\^\^\^\^\^\^\^ ..
list-table:

    * - **Metric**
      - | The percentage of completeness of the unique password policy
    * - **Calculation**
      - :code:`(M2 + M4) / 2`

### Strength of Policy

+-----------------+---------------------------------------------------+
| **Metric**      | | The percentage of password guidance that meets  |
|                 |   minimum character length                        |
|                 | | standards                                       |
+-----------------+---------------------------------------------------+
| **Calculation** | `(M3 + M5) / 2`                                   |
+-----------------+---------------------------------------------------+
