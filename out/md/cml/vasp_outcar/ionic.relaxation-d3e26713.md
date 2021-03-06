# ionic.relaxation {#ionic.relaxation-d3e26713}

VASP outcar

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Partial.png)                                                                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | VASP outcar                                                                                                                                                                                           |
| id                                                                                                                                                                                                    | ionic.relaxation                                                                                                                                                                                      |
| name                                                                                                                                                                                                  | Ionic relaxation section                                                                                                                                                                              |
| pattern                                                                                                                                                                                               | \\s\*Ionic\\srelaxation.\*                                                                                                                                                                            |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | ionic.relaxation.xml                                                                                                                                                                                  |

######Template attributes

**Input.**

     Ionic relaxation
       EDIFFG = 0.1E-03   stopping-criterion for IOM
       NSW    =    600    number of steps for IOM
       NBLOCK =      1;   KBLOCK =    600    inner block; outer block 
       IBRION =     44    ionic relax: 0-MD 1-quasi-New 2-CG
       NFREE  =      0    steps in history (QN), initial steepest desc. (CG)
       ISIF   =      2    stress and relaxation
       IWAVPR =     11    prediction:  0-non 1-charg 2-wave 3-comb
       ISYM   =      2    0-nonsym 1-usesym 2-fastsym
       LCORR  =      T    Harris-Foulkes like correction to forces
        
        

**Output text.**

```xml
<comment class="example.output" id="ionic.relaxation">
        <module cmlx:templateRef="ionic.relaxation">
            <module>
                <list cmlx:templateRef="missingID">
                    <scalar dataType="xsd:double" dictRef="v:ediffg">0.1E-03</scalar>
                </list>
            </module>
            <module>
                <list cmlx:templateRef="missingID">
                    <scalar dataType="xsd:integer" dictRef="v:ibrion">44</scalar>
                </list>
            </module>
        </module>
    </comment>
```
