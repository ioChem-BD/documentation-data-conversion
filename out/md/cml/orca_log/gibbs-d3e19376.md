# gibbs {#gibbs-d3e19376}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | gibbs                                                                                                                                               |
| name                                                                                                                                                | Gibbs free enthalpy                                                                                                                                 |
| pattern                                                                                                                                             | \\s\*-{10,}\\s\*\$\\s\*GIBBS\\sFREE\\sENTHALPY\\s\*                                                                                                 |
| endPattern                                                                                                                                          | \\s\*G-E\\(el\\).\*                                                                                                                                 |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | 1                                                                                                                                                   |
| keep                                                                                                                                                | last                                                                                                                                                |
| xml:base                                                                                                                                            | gibbs.xml                                                                                                                                           |

######Template attributes

**Input.**

    -------------------
    GIBBS FREE ENTHALPY
    -------------------

    The Gibbs free enthalpy is G = H - T*S

    Total enthalpy                    ...   -228.85953707 Eh
    Total entropy correction          ...     -0.03181461 Eh    -19.96 kcal/mol
    -----------------------------------------------------------------------
    Final Gibbs free enthalpy         ...   -228.89135168 Eh

    For completeness - the Gibbs free enthalpy minus the electronic energy
    G-E(el)                           ...      0.03360703 Eh     21.09 kcal/mol
        
        

**Output text.**

```xml
<comment class="example.output" id="gibbs">   
         <module cmlx:templateRef="gibbs">
           <scalar dataType="xsd:double" dictRef="o:totalenthalpy" units="nonsi:hartree">-228.85953707</scalar>
           <scalar dataType="xsd:double" dictRef="o:totalentropycorr" units="nonsi:hartree">-0.03181461</scalar>
           <scalar dataType="xsd:double" dictRef="o:gibbsenthalpy" units="nonsi:hartree">-228.89135168</scalar>
           <scalar dataType="xsd:double" dictRef="o:gibbsminuselec" units="nonsi:hartree">0.03360703</scalar>
        </module>
    </comment>
```
