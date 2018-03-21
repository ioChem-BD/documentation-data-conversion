# energy {#energy-d3e25158}

Turbomole log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole log                                                                                                                                       |
| id                                                                                                                                                  | energy                                                                                                                                              |
| name                                                                                                                                                | Final energies section                                                                                                                              |
| pattern                                                                                                                                             | \\s\*\\\*{10,}\\s\*\$\\s\*\\\*\\s\*\\\*\\s\*\$\\s\*\\\*\\s+RHF\\s+energy.\*                                                                         |
| endPattern                                                                                                                                          | \\s\*\\\*{10,}\\s\*                                                                                                                                 |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | energy.xml                                                                                                                                          |

######Template attributes

**Input.**

          *********************************************************************
          *                                                                   *
          *  RHF  energy                             :   -227.9061850367      *
          *  CCSD correlation energy                 :     -0.8835141933      *
          *  E4 doubles and triples contribution     :     -0.0356016214      *
          *  E5 singles and triples contribution     :      0.0019555922      *
          *  total correlation energy                :     -0.9171602226      *
          *                                                                   *
          *  Final CCSD(T) energy                    :   -228.8233452593      *
          *                                                                   *
          *  D1 diagnostic (CCSD)                    :      0.0560            *
          *                                                                   *
          *********************************************************************
        

**Input.**

          *********************************************************************
          *                                                                   *
          *  RHF  energy                             :   -227.9061850367      *
          *  MP2 correlation energy (doubles)        :     -0.8639282496      *
          *                                                                   *
          *  Final MP2 energy                        :   -228.7701132863      *
          *                                                                   *
          *   E(S)   =     -0.5531547215      E(T)   =     -0.3107735281      *
          *   E(OS)  =     -0.6567458975      E(SS)  =     -0.2071823521      *
          *                                                                   *
          *  SCS-MP2 energy                          :   -228.7633408977      *
          *  (computed with  C(OS) =   1.2000  and  C(SS) =   0.3333)         *
          *                                                                   *
          *  SOS-MP2 energy                          :   -228.7599547035      *
          *  (computed with  C(OS) =   1.3000)                                *
          *                                                                   *
          *  Norm of MP1 T2 amplitudes               :      0.2766656730      *
          *                                                                   *
          ********************************************************************* 
        

**Input.**

          *********************************************************************
          *                                                                   *
          *  RHF  energy                             :   -227.9061850367      *
          *  correlation energy                      :     -0.8835141933      *
          *                                                                   *
          *  Final CCSD energy                       :   -228.7896992300      *
          *                                                                   *
          *  D1 diagnostic                           :      0.0560            *
          *                                                                   *
          ********************************************************************* 
        

**Output text.**

```xml
<comment class="example.output" id="energy">
         <module cmlx:templateRef="energy">
           <scalar dataType="xsd:double" dictRef="t:rhfEnergy" units="nonsi:hartree">-227.9061850367</scalar>
            <module dictRef="CCSD(T)">
               <scalar dataType="xsd:double" dictRef="t:finalEnergy" units="nonsi:hartree">-228.8233452593</scalar>
            </module>
            <scalar dataType="xsd:double" dictRef="t:d1diagnostic">0.0560</scalar>
         </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="energy2">
         <module cmlx:templateRef="energy">
            <scalar dataType="xsd:double" dictRef="t:rhfEnergy" units="nonsi:hartree">-227.9061850367</scalar>
            <module dictRef="MP2">
               <scalar dataType="xsd:double" dictRef="t:finalEnergy" units="nonsi:hartree">-228.7701132863</scalar>
            </module>
         </module>            
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="energy3">
         <module cmlx:templateRef="energy">
            <scalar dataType="xsd:double" dictRef="t:rhfEnergy" units="nonsi:hartree">-227.9061850367</scalar>
            <module dictRef="CCSD">
               <scalar dataType="xsd:double" dictRef="t:finalEnergy" units="nonsi:hartree">-228.7896992300</scalar>
            </module>
         </module>
    </comment>
```
