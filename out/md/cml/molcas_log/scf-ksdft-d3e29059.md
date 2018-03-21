# scf-ksdft {#scf-ksdft-d3e29059}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | scf-ksdft                                                                                                                                           |
| name                                                                                                                                                | scf-ksdft                                                                                                                                           |
| pattern                                                                                                                                             | .\*\$.\*\$\\s\*\\\*\\s+SCF\\/KS-DFT\\sProgram,\\sFinal\\sresults.\*                                                                                 |
| endPattern                                                                                                                                          | .\*\[0-9\]\$\\s\*                                                                                                                                   |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/scf.ksdft.xml                                                                                                                               |

######Template attributes

**Input.**

     *****************************************************************************************************************************
     *                                                                                                                           *
     *                                             SCF/KS-DFT Program, Final results                                             *
     *                                                                                                                           *
     *                                                                                                                           *
     *                                                                                                                           *
     *                                                       Final Results                                                       *
     *                                                                                                                           *
     *****************************************************************************************************************************

    ::    Total KS-DFT energy                            -228.9933944011
          One-electron energy                            -578.7912410526
          Two-electron energy                             229.6062654451
          Nuclear repulsion energy                        120.1915812063
          Kinetic energy (interpolated)                   228.0908173117
          Virial theorem                                    1.0039570952
          Total spin, S(S+1)                                0.0000000000
          Total spin, S                                     0.0000000000
          Max non-diagonal density matrix element           0.0000000000
          Max non-diagonal Fock matrix element              0.0000009824
        
        

**Output text.**

```xml
<comment class="example.output" id="scf-ksdft">
        <module cmlx:templateRef="scf-ksdft">
            <scalar dataType="xsd:string" dictRef="m:program">KS-DFT</scalar>
            <scalar dataType="xsd:double" dictRef="m:scfener">-228.9933944011</scalar>
            <scalar dataType="xsd:double" dictRef="m:oneelectener">-578.7912410526</scalar>
            <scalar dataType="xsd:double" dictRef="m:twoelectener">229.6062654451</scalar>
            <scalar dataType="xsd:double" dictRef="cc:nucrepener">120.1915812063</scalar>
            <scalar dataType="xsd:double" dictRef="m:kineticener">228.0908173117</scalar>
            <scalar dataType="xsd:double" dictRef="m:virial">1.0039570952</scalar>
            <scalar dataType="xsd:double" dictRef="m:spin">0.0000000000</scalar>
            <scalar dataType="xsd:double" dictRef="m:matrixdensityelem">0.0000000000</scalar>
            <scalar dataType="xsd:double" dictRef="m:matrixfockelement">0.0000009824</scalar>
        </module> 
    </comment>
```
