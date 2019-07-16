# coupledClusterEnergy {#coupledClusterEnergy-d3e22175}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Partial.png)                                                                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Orca log                                                                                                                                                                                              |
| id                                                                                                                                                                                                    | coupledClusterEnergy                                                                                                                                                                                  |
| pattern                                                                                                                                                                                               | \\s\*-{15,}\$\\s\*COUPLED\\sCLUSTER\\sENERGY\\s\*                                                                                                                                                     |
| endPattern                                                                                                                                                                                            | \\s\*\$\\s\*-{15,}                                                                                                                                                                                    |
| endPattern2                                                                                                                                                                                           | \\s\*\\\*{20,}\\s\*                                                                                                                                                                                   |
| endPattern3                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | coupledcluster.xml                                                                                                                                                                                    |

######Template attributes

**Input.**

    ----------------------
    COUPLED CLUSTER ENERGY
    ----------------------

    E(0)                                       ...   -227.635883412
    E(CORR)                                    ...     -0.665826163
    E(TOT)                                     ...   -228.301709575
    Singles Norm <SIS>**1/2                    ...      0.074835151
    T1 diagnostic                              ...      0.015275661

    ------------------
        

**Output text.**

```xml
<comment class="example.output" id="coupledClusterEnergy">
        <module cmlx:templateRef="coupledClusterEnergy">
            <scalar dataType="xsd:double" dictRef="o:t1diag">0.015275661</scalar>
        </module> 
    </comment>
```
