# eprnmr {#eprnmr-d3e21993}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | eprnmr                                                                                                                                              |
| name                                                                                                                                                | EPR/NMR calculation section                                                                                                                         |
| pattern                                                                                                                                             | \\s\*ORCA\\sEPR\\/NMR\\s\*CALCULATION\\s\*                                                                                                          |
| endPattern                                                                                                                                          | \\s\*DOMO-.VMO.\*                                                                                                                                   |
| endPattern2                                                                                                                                         | \\s\*\\\*{20,}.\*                                                                                                                                   |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | eprnmr/eprnmr.xml                                                                                                                                   |

######Template attributes

**Comment.**

    ------------------------------------------------------------------------------
                                    ORCA EPR/NMR CALCULATION
    ------------------------------------------------------------------------------
    ...

    DOMO->SOMO (beta ->beta )  :     0.917      1.080
    SOMO->SOMO (alpha->beta )  :    -0.029     -0.343
    DOMO->VMO  (beta ->alpha)  :    -0.122      0.022
        
