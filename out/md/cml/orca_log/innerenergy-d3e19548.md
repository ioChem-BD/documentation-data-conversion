# innerenergy {#innerenergy-d3e19548}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Orca log                                                                                                                                                                                              |
| id                                                                                                                                                                                                    | innerenergy                                                                                                                                                                                           |
| name                                                                                                                                                                                                  | Inner energy                                                                                                                                                                                          |
| pattern                                                                                                                                                                                               | \\s\*-{10,}\$\\s\*INNER\\sENERGY                                                                                                                                                                      |
| endPattern                                                                                                                                                                                            | \\s\*Total\\scorrection.\*                                                                                                                                                                            |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| keep                                                                                                                                                                                                  | last                                                                                                                                                                                                  |
| xml:base                                                                                                                                                                                              | innerenergy.xml                                                                                                                                                                                       |

######Template attributes

**Input.**

    ------------
    INNER ENERGY
    ------------

    The inner energy is: U= E(el) + E(ZPE) + E(vib) + E(rot) + E(trans)
        E(el)   - is the total energy from the electronic structure calculation
                  = E(kin-el) + E(nuc-el) + E(el-el) + E(nuc-nuc)
        E(ZPE)  - the the zero temperature vibrational energy from the frequency calculation
        E(vib)  - the the finite temperature correction to E(ZPE) due to population
                  of excietd vibrational states
        E(rot)  - is the rotational thermal energy
        E(trans)- is the translational thermal energy

    Summary of contributions to the inner energy U:
    Electronic energy                ...   -228.92495871 Eh
    Zero point energy                ...      0.05984322 Eh      37.55 kcal/mol
    Thermal vibrational correction   ...      0.00180167 Eh       1.13 kcal/mol
    Thermal rotational correction    ...      0.00141627 Eh       0.89 kcal/mol
    Thermal translational correction ...      0.00141627 Eh       0.89 kcal/mol
    -----------------------------------------------------------------------
    Total thermal energy                   -228.86048127 Eh


    Summary of corrections to the electronic energy:
    (perhaps to be used in another calculation)
    Total thermal correction                  0.00463421 Eh       2.91 kcal/mol
    Non-thermal (ZPE) correction              0.05984322 Eh      37.55 kcal/mol
    -----------------------------------------------------------------------
    Total correction                          0.06447743 Eh      40.46 kcal/mol


    --------    
        

**Output text.**

```xml
<comment class="example.output" id="innerenergy">
        <module cmlx:templateRef="innerenergy">
            <module cmlx:templateRef="contributions">
               <scalar dataType="xsd:double" dictRef="o:electronic" units="nonsi:hartree">-228.92495871</scalar>
               <scalar dataType="xsd:double" dictRef="o:zeropoint" units="nonsi:hartree">0.05984322</scalar>
               <scalar dataType="xsd:double" dictRef="o:thermalvibcorrection" units="nonsi:hartree">0.00180167</scalar>
               <scalar dataType="xsd:double" dictRef="o:thermalrotcorrection" units="nonsi:hartree">0.00141627</scalar>
               <scalar dataType="xsd:double" dictRef="o:thermaltrasncorrection" units="nonsi:hartree">0.00141627</scalar>
               <scalar dataType="xsd:double" dictRef="o:thermaltotal" units="nonsi:hartree">-228.86048127</scalar>
            </module>
            <module cmlx:templateRef="corrections">
               <scalar dataType="xsd:double" dictRef="o:thermalcorr" units="nonsi:hartree">0.00463421</scalar>
               <scalar dataType="xsd:double" dictRef="o:nonthermalcorr" units="nonsi:hartree">0.05984322</scalar>
               <scalar dataType="xsd:double" dictRef="o:totalcorr" units="nonsi:hartree">0.06447743</scalar>
            </module>
        </module>
    </comment>
```
