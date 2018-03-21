# energies {#energies-d3e32917}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | QuantumEspresso log                                                                                                                                 |
| id                                                                                                                                                  | energies                                                                                                                                            |
| name                                                                                                                                                | Energy section                                                                                                                                      |
| pattern                                                                                                                                             | \\s\*the\\sFermi\\senergy\\sis.\*                                                                                                                   |
| endPattern                                                                                                                                          | \\s\*absolute\\smagnetization.\*                                                                                                                    |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | energies.xml                                                                                                                                        |

######Template attributes

**Input.**

         the Fermi energy is     1.2269 ev

    !    total energy              =  -14856.08746891 Ry
         Harris-Foulkes estimate   =  -14856.08746891 Ry
         estimated scf accuracy    <          9.5E-10 Ry

         The total energy is the sum of the following terms:

         one-electron contribution = -145858.09904553 Ry
         hartree contribution      =   73114.21474057 Ry
         xc contribution           =   -1873.98188981 Ry
         ewald contribution        =   59756.12730301 Ry
         Dispersion Correction     =      -1.71103674 Ry
         Hubbard energy            =       7.44204694 Ry
         smearing contrib. (-TS)   =      -0.07958735 Ry

         total magnetization       =     0.00 Bohr mag/cell
         absolute magnetization    =   198.74 Bohr mag/cell 
        

**Output text.**

```xml
<comment class="example.output" id="energies">
        <module cmlx:templateRef="energies">
            <scalar dataType="xsd:double" dictRef="qex:fermiener" units="nonsi:electronvolt">1.2269</scalar>
            <scalar dataType="xsd:double" dictRef="qex:totalener" units="nonsi:electronvolt">-202127,440544</scalar>
            <scalar dataType="xsd:double" dictRef="qex:harrisfoulkes" units="nonsi:electronvolt">-202127,440544</scalar>
            <scalar dataType="xsd:string" dictRef="qex:sscfaccuracy" units="nonsi:electronvolt">0,000000</scalar>
            <scalar dataType="xsd:double" dictRef="qex:oneelec" units="nonsi:electronvolt">-1984501,256094</scalar>
            <scalar dataType="xsd:double" dictRef="qex:hartee" units="nonsi:electronvolt">994769,930093</scalar>
            <scalar dataType="xsd:double" dictRef="qex:xc" units="nonsi:electronvolt">-25496,831774</scalar>
            <scalar dataType="xsd:double" dictRef="qex:ewald" units="nonsi:electronvolt">813023,825678</scalar>
            <scalar dataType="xsd:double" dictRef="qex:dispcorr" units="nonsi:electronvolt">-23,279849</scalar>
            <scalar dataType="xsd:double" dictRef="qex:hubbardener" units="nonsi:electronvolt">101,254244</scalar>
            <scalar dataType="xsd:double" dictRef="qex:totalmag" units="bohrmag.cell-1">0.00</scalar>
            <scalar dataType="xsd:double" dictRef="cc:absolutemag" units="bohrmag.cell-1">198.74</scalar>
        </module>
    </comment>
```
