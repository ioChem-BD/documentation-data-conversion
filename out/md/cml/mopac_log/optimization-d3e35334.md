# optimization {#optimization-d3e35334}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOPAC log                                                                                                                                           |
| id                                                                                                                                                  | optimization                                                                                                                                        |
| name                                                                                                                                                | Geometry optimization                                                                                                                               |
| pattern                                                                                                                                             | .\*\\sGeometry\\soptimization\\susing.\*                                                                                                            |
| endPattern                                                                                                                                          | \\s\*COMPUTATION\\sTIME.\*                                                                                                                          |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | optimization.xml                                                                                                                                    |

######Template attributes

-   [geometry](/out/md/cml/mopac_log/geometry-d3e35338.md)

<!-- -->

-   [energies](/out/md/cml/mopac_log/energies-d3e35473.md)

<!-- -->

-   [jobcpu](/out/md/cml/mopac_log/jobcpu-d3e35603.md)


