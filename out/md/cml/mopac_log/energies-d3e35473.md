# energies {#energies-d3e35473}

MOPAC log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOPAC log                                                                                                                                           |
| id                                                                                                                                                  | energies                                                                                                                                            |
| name                                                                                                                                                | Energies section                                                                                                                                    |
| pattern                                                                                                                                             | .\*\\sTOTAL\\sENERGY\\s\*=.\*                                                                                                                       |
| pattern2                                                                                                                                            | \\s\*ZERO\\sPOINT\\sENERGY.\*                                                                                                                       |
| endPattern                                                                                                                                          | \\s\*SCF\\sCALCULATIONS.\*                                                                                                                          |
| endPattern2                                                                                                                                         | \\s\*WALL-CLOCK\\sTIME.\*                                                                                                                           |
| endPattern3                                                                                                                                         | \\s\*NORMAL\\sCOORDINATE\\sANALYSIS.\*                                                                                                              |
| endPattern4                                                                                                                                         | \\s\*CARTESIAN\\sCOORDINATE\\sDERIVATIVES.\*                                                                                                        |
| endPattern5                                                                                                                                         | \\s\*NORMAL\\sCOORDINATE\\sANALYSIS.\*                                                                                                              |
| endPattern6                                                                                                                                         | \\s\*GRADIENT\\s+NORM.\*                                                                                                                            |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | energies.xml                                                                                                                                        |

######Template attributes

**Input.**

              TOTAL ENERGY            =   -3024354.64134 KCAL/MOL
              ENERGY OF ATOMS         =    3019975.06610 KCAL/MOL
                                  SUM =      -4379.57525 KCAL/MOL
              DISPERSION ENERGY       =          0.00000 KCAL/MOL
              MM CORRECTION FOR >N-   =        -10.86572 KCAL/MOL
                                  SUM =      -4390.44097 KCAL/MOL

     WARNING - An energy term is missing!


              TOTAL ENERGY            =    -131148.53702 EV
              ELECTRONIC ENERGY       =   -7116479.16086 EV
              CORE-CORE REPULSION     =    6985330.62384 EV

              GRADIENT NORM           =          3.24521
        

**Input.**

              ZERO POINT ENERGY      59.540 KCAL/MOL


               NORMAL COORDINATE ANALYSIS (Total motion = 1 Angstrom)   
        

**Output text.**

```xml
<comment class="example.output" id="energies">
        <module cmlx:templateRef="energies">
            <scalar dataType="xsd:double" dictRef="mp:atomener" units="nonsi:hartree">4812.63226533696</scalar>
            <scalar dataType="xsd:double" dictRef="mp:dispenergy" units="nonsi:hartree">0.0</scalar>
            <scalar dataType="xsd:double" dictRef="mp:mmcorrectionforn" units="nonsi:hartree">-0.017315611392</scalar>
            <scalar dataType="xsd:double" dictRef="mp:totalsum" units="nonsi:hartree">-6.996606729791999</scalar>
            <scalar dataType="xsd:double" dictRef="cc:totalener" units="nonsi:hartree">-4819.618085616211</scalar>
            <scalar dataType="xsd:string" dictRef="cc:electener" units="nonsi:hartree">-261525.69025120902</scalar>
            <scalar dataType="xsd:double" dictRef="cc:nucrepener" units="nonsi:hartree">256706.07216559278</scalar>
         </module>         
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="energies2">
        <module cmlx:templateRef="energies">
               <scalar dataType="xsd:double" dictRef="cc:zeropoint" units="nonsi:hartree">0.094882944</scalar>
        </module>
    </comment>
```
