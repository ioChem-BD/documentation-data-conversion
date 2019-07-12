# restricted.orbitals {#restricted.orbitals-d3e25466}

Turbomole log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole log                                                                                                                                       |
| id                                                                                                                                                  | restricted.orbitals                                                                                                                                 |
| name                                                                                                                                                | Molecular orbitals (restricted)                                                                                                                     |
| pattern                                                                                                                                             | \\s\*orbitals.\*scfmo\\s\*will\\sbe\\swritten\\sto\\sfile.\*                                                                                        |
| endPattern                                                                                                                                          | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| xml:base                                                                                                                                            | restricted.orbitals.xml                                                                                                                             |

######Template attributes

**Input.**

     orbitals $scfmo  will be written to file mos

        irrep                 18ag        19ag        20ag        21ag        22ag  
     eigenvalues H         -0.59748    -0.57961    -0.54752    -0.54279    -0.45030
                eV         -16.2584    -15.7721    -14.8988    -14.7703    -12.2535
     occupation              2.0000      2.0000      2.0000      2.0000      2.0000 

        irrep                 23ag        24ag        25ag        26ag        27ag  
     eigenvalues H         -0.24507    -0.23232    -0.17908    -0.13662    -0.11917
                eV          -6.6687     -6.3217     -4.8729     -3.7178     -3.2427

        irrep                 34eg        35eg        36eg        37eg        38eg  
     eigenvalues H         -0.55232    -0.53899    -0.53899    -0.45926    -0.45926
                eV         -15.0295    -14.6668    -14.6668    -12.4972    -12.4972
     occupation              2.0000      2.0000      2.0000      2.0000      2.0000 

        irrep                 39eg        40eg        41eg        42eg        43eg  
     eigenvalues H         -0.25774    -0.25774    -0.23812    -0.23812    -0.22318
                eV          -7.0135     -7.0135     -6.4796     -6.4796     -6.0732

        irrep                 16au        17au        18au        19au        20au  
     eigenvalues H         -0.63839    -0.57973    -0.56239    -0.55584    -0.53607
                eV         -17.3717    -15.7755    -15.3037    -15.1253    -14.5873
     occupation              2.0000      2.0000      2.0000      2.0000      2.0000 

        irrep                 21au        22au        23au        24au        25au  
     eigenvalues H         -0.25094    -0.24229    -0.16523    -0.13696    -0.11172
                eV          -6.8284     -6.5931     -4.4961     -3.7270     -3.0402

        irrep                 36eu        37eu        38eu        39eu        40eu  
     eigenvalues H         -0.56814    -0.54779    -0.54779    -0.53708    -0.53708
                eV         -15.4599    -14.9063    -14.9063    -14.6149    -14.6149
     occupation              2.0000      2.0000      2.0000      2.0000      2.0000 

        irrep                 41eu        42eu        43eu        44eu        45eu  
     eigenvalues H         -0.25132    -0.25132    -0.23207    -0.23207    -0.16750
                eV          -6.8388     -6.8388     -6.3150     -6.3150     -4.5579

        

> **Warning**
>
> Current template has input comments defined but it's output is missing, please notify software developers.

## orbital.line {#orbital.line-d3e25475}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole log                                                                                                                                       |
| id                                                                                                                                                  | orbital.line                                                                                                                                        |
| pattern                                                                                                                                             | \\s\*irrep.\*                                                                                                                                       |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | orbital.line.xml                                                                                                                                    |

######Template attributes

**Input.**

            irrep                  1a1'        2a1'        3a1'        4a1'        5a1' 
     eigenvalues H       -256.02776   -29.97174   -10.18645    -3.38954    -0.88456
                eV       -6966.9251   -815.5790   -277.1896    -92.2348    -24.0702
     occupation              2.0000      2.0000      2.0000      2.0000      2.0000 
        

**Output text.**

```xml
<comment class="example.output" id="orbital.line">
      <module cmlx:lineCount="5" cmlx:templateRef="orbital">
          <array dataType="xsd:string" size="5" dictRef="cc:irrep">1a1' 2a1' 3a1' 4a1' 5a1'</array>
          <array dataType="xsd:double" size="5" dictRef="t:eigen">-256.02776 -29.97174 -10.18645 -3.38954 -0.88456</array>
          <array dataType="xsd:double" size="5" dictRef="t:orbitalenergy">-6966.9251 -815.579 -277.1896 -92.2348 -24.0702</array>
          <array dataType="xsd:double" size="5" dictRef="cc:occupation">2.0000 2.0000 2.0000 2.0000 2.0000</array>
      </module>
    
    
    </comment>
```
