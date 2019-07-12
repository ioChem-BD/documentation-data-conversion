# adf.computation {#adf.computation-d3e1999}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | adf.computation                                                                                                                                     |
| pattern                                                                                                                                             | \\s+\\\*\\s+C\\sO\\sM\\sP\\sU\\sT\\sA\\sT\\sI\\sO\\sN\\s+\\\*.\*                                                                                    |
| endPattern                                                                                                                                          | \\s\*\\d\*\\s\*\$\\s\\\*{20,}.\*\$(\\s\*I\\s\*LOGFILE.\*)                                                                                           |
| offset                                                                                                                                              | -1                                                                                                                                                  |
| endOffset                                                                                                                                           | 2                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | computation/computation.xml                                                                                                                         |

######Template attributes

**Comment.**

                                                ***************************
                                                *  C O M P U T A T I O N  *
                                                ***************************
     
     =====
     S C F
     ===== 
     ...
     
     Geometry CYCLE N
     ==============
     ...
     
     =============================
     G E O M E T R Y   U P D A T E  ***  1  ***
     =============================
     ...
        
     
     ***************************************************************************************************
        
        

-   [scf](/out/md/cml/adf_log/scf-d3e2006.md)

<!-- -->

-   [geometry.cycle](/out/md/cml/adf_log/geometry.cycle-d3e2037.md)


