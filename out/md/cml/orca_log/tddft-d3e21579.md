# tddft {#tddft-d3e21579}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | tddft                                                                                                                                               |
| name                                                                                                                                                | TDDFT calculation                                                                                                                                   |
| pattern                                                                                                                                             | \\s\*-{40,}\\s\*\$\\s\*ORCA\\s(TD-DFT(/TDA)?ICIS)\\sCALCULATION.\*                                                                                  |
| endPattern                                                                                                                                          | \\s\*\\\*\\\*\\\*\\sORCA-CIS/TD-DFT\\sFINISHED\\sWITHOUT\\sERROR\\s\\\*\\\*\\\*\\s\*                                                                |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | tddft/tddft.xml                                                                                                                                     |

######Template attributes

-   [excitedstates](/out/md/cml/orca_log/excitedstates-d3e21583.md)

<!-- -->

-   [absorptionspec](/out/md/cml/orca_log/absorptionspec-d3e21910.md)


