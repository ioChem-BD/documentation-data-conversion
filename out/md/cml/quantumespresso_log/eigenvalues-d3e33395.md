# eigenvalues {#eigenvalues-d3e33395}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | QuantumEspresso log                                                                                                                                 |
| id                                                                                                                                                  | eigenvalues                                                                                                                                         |
| name                                                                                                                                                | Eigenvalues resume                                                                                                                                  |
| pattern                                                                                                                                             | \\s\*------\\s\*SPIN\\sUP\\s\*------------.\*                                                                                                       |
| endPattern                                                                                                                                          | \\s\*\$\\s\*the\\sFermi\\senergy\\sis.\*                                                                                                            |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| keep                                                                                                                                                | last                                                                                                                                                |
| xml:base                                                                                                                                            | eigenvalues.xml                                                                                                                                     |

######Template attributes


