# enthalpy {#enthalpy-d3e19457}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | enthalpy                                                                                                                                            |
| name                                                                                                                                                | Enthalpy section                                                                                                                                    |
| pattern                                                                                                                                             | \\s\*-{5,}\\s\*\$\\s\*ENTHALPY\\s\*                                                                                                                 |
| endPattern                                                                                                                                          | \\s\*Total\\sEnthalpy.\*                                                                                                                            |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | enthalpy.xml                                                                                                                                        |

######Template attributes

**Input.**

    --------
    ENTHALPY
    --------

    The enthalpy is H = U + kB*T
                    kB is Boltzmann's constant
    Total free energy                 ...   -228.86048127 Eh
    Thermal Enthalpy correction       ...      0.00094421 Eh       0.59 kcal/mol
    -----------------------------------------------------------------------
    Total Enthalpy                    ...   -228.85953707 Eh    
        

**Output text.**

```xml
<comment class="example.output" id="enthalpy">
        <module cmlx:templateRef="enthalpy">
            <scalar dataType="xsd:double" dictRef="o:totalfree" units="nonsi:hartree">-228.86048127</scalar>
            <scalar dataType="xsd:double" dictRef="o:thermalcorrenthalpy" units="nonsi:hartree">0.00094421</scalar>
            <scalar dataType="xsd:double" dictRef="o:totalenthalpy" units="nonsi:hartree">-228.85953707</scalar>
        </module>
    </comment>
```
