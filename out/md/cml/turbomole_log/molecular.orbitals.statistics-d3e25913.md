# molecular.orbitals.statistics {#molecular.orbitals.statistics-d3e25913}

Turbomole log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole log                                                                                                                                                                                         |
| id                                                                                                                                                                                                    | molecular.orbitals.statistics                                                                                                                                                                         |
| name                                                                                                                                                                                                  | Molecular orbital statistic section                                                                                                                                                                   |
| pattern                                                                                                                                                                                               | \\s\*Molecular\\sOrbital\\sStatistic:\\s\*                                                                                                                                                            |
| endPattern                                                                                                                                                                                            | \\s\*all\\stogether\\s\*:.\*\$\\s\*-{20,}\\s\*                                                                                                                                                        |
| endOffset                                                                                                                                                                                             | 2                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | molecularorbitals/molecular.orbital.statistic.xml                                                                                                                                                     |

######Template attributes

**Input.**

       Molecular Orbital Statistic:
       ============================


       ---------------------
        irred. repres.:    a
       ---------------------
       frozen occupied:    0
       active occupied:   16
       active virtual :  132
       frozen virtual :    0
       ---------------------


       -----------------------------
       orbitals in total:
       -----------------------------
        frozen occupied :      0
        active occupied :     16
        active virtual  :    132
        frozen virtual  :      0
        all together    :    148
       -----------------------------    
        

**Output text.**

```xml
<comment class="example.output" name="molecular.orbitals.statistics">
        <module cmlx:templateRef="molecular.orbitals.statistics">
            <scalar dataType="xsd:integer" dictRef="t:frozenocc">0</scalar>
            <scalar dataType="xsd:integer" dictRef="t:activeocc">16</scalar>
            <scalar dataType="xsd:integer" dictRef="t:activevirt">132</scalar>
            <scalar dataType="xsd:integer" dictRef="t:frozenvirt">0</scalar>
            <scalar dataType="xsd:integer" dictRef="t:orbitalsum">148</scalar>
        </module>   
   </comment>
```
