# statistics {#statistics-d3e4394}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | ADF log                                                                                                                                                                                               |
| id                                                                                                                                                                                                    | statistics                                                                                                                                                                                            |
| name                                                                                                                                                                                                  | Final statistics resume                                                                                                                                                                               |
| pattern                                                                                                                                                                                               | \\s\*Timing\\sStatistics.\*                                                                                                                                                                           |
| endPattern                                                                                                                                                                                            | \\s\*\\\*{20,}+.\*                                                                                                                                                                                    |
| offset                                                                                                                                                                                                | -1                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | statistics/statistics.xml                                                                                                                                                                             |

######Template attributes

**Comment.**

     =================
     Timing Statistics
     =================

     Total Used :                     CPU=        0.32      System=        0.16     Elapsed=        1.05
    ...

     ***************************************************************************************************
        

-   [timing](/out/md/cml/adf_log/timing-d3e4401.md)


