# loprop {#loprop-d3e30308}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | loprop                                                                                                                                              |
| name                                                                                                                                                | LoProp population analysis                                                                                                                          |
| pattern                                                                                                                                             | \\s\*LoProp\\spopulation\\sAnalysis\\sfor\\sroot\\snumber.\*                                                                                        |
| pattern2                                                                                                                                            | \\s\*LoProp\\sCharges\\sper\\scenter.\*                                                                                                             |
| endPattern                                                                                                                                          | \\s\*Total.\*\$\\s\*\$\\s{0,10}\\S+.\*                                                                                                              |
| endPattern2                                                                                                                                         | \\s\*\\-\\-\\s\*                                                                                                                                    |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/loprop.xml                                                                                                                                  |

######Template attributes

**Input.**

          LoProp population Analysis for root number: 1
          -----------------------------------------------


          LoProp Charges per center                                                                                               


                       N1       N2       O1       O2       C1       C2       C3       C4       H1       H2  
          Nuclear      7.0000   7.0000   8.0000   8.0000   6.0000   6.0000   6.0000   6.0000   1.0000   1.0000
          Electronic  -6.7339  -6.7346  -8.5323  -8.5324  -5.8535  -6.1062  -5.8540  -6.1068  -0.8480  -0.8520

          Total        0.2661   0.2654  -0.5323  -0.5324   0.1465  -0.1062   0.1460  -0.1068   0.1520   0.1480


                       H3       H4  
          Nuclear      1.0000   1.0000
          Electronic  -0.8479  -0.8523

          Total        0.1521   0.1477

          Natural Bond Order Analysis for root number: 1
        

**Input.**

> **Warning**
>
> Current template has input comments defined but it's output is missing, please notify data architects.
