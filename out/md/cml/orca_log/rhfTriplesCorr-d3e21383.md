# rhfTriplesCorr {#rhfTriplesCorr-d3e21383}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | rhfTriplesCorr                                                                                                                                      |
| pattern                                                                                                                                             | \\s\*-{15,}\$\\s\*RHF\\sTRIPLES\\sCORRECTION.\*                                                                                                     |
| endPattern                                                                                                                                          | \\s\*W\\(HF\\)                                                                                                                                      |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | rhftriplescorr.xml                                                                                                                                  |

######Template attributes

**Input.**

    ----------------------
    RHF TRIPLES CORRECTION (Algorithm 1)
    ----------------------

    Multiplier for the singles contribution    ...      1.000000000

    10% done
    20% done
    30% done
    40% done
    50% done
    60% done
    70% done
    80% done
    90% done

    Triples Correction (T)                     ...     -0.019986933
    Final correlation energy                   ...     -0.685813096
    E(CCSD)                                    ...   -228.301709575
    E(CCSD(T))                                 ...   -228.321696508

    NORM  =      1.221657626 sqrt=     1.105286219
    W(HF) =      0.818559946
        

**Output text.**

```xml
<comment class="example.output" id="rhfTriplesCorr">
        <module cmlx:templateRef="rhfTriplesCorr">
           <scalar dataType="xsd:double" dictRef="o:tripCorr" units="nonsi:hartree">-0.019986933</scalar>
           <scalar dataType="xsd:double" dictRef="o:finCorrEner" units="nonsi:hartree">-0.685813096</scalar>
           <scalar dataType="xsd:double" dictRef="o:ccsdEner" units="nonsi:hartree">-228.301709575</scalar>
           <scalar dataType="xsd:double" dictRef="o:ccsdtEner" units="nonsi:hartree">-228.321696508</scalar>
        </module>
    </comment>
```
