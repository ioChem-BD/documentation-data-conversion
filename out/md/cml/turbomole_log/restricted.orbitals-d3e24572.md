# restricted.orbitals {#restricted.orbitals-d3e24572}

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
| endPattern                                                                                                                                          | \\s\*\$\\s\*                                                                                                                                        |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| xml:base                                                                                                                                            | restricted.orbitals.xml                                                                                                                             |

######Template attributes

**Input.**

         orbitals $scfmo  will be written to file mos

        irrep                  1a1'        2a1'        3a1'        4a1'        5a1' 
     eigenvalues H       -256.02776   -29.97174   -10.18645    -3.38954    -0.88456
                eV       -6966.9251   -815.5790   -277.1896    -92.2348    -24.0702
     occupation              2.0000      2.0000      2.0000      2.0000      2.0000

        irrep                  6a1'        7a1'        8a1'        9a1'       10a1' 
     eigenvalues H         -0.52760    -0.40581    -0.22513     0.04248     0.15326
                eV         -14.3569    -11.0428     -6.1262      1.1561      4.1703
     occupation              2.0000      2.0000      2.0000

        irrep                 21e2" 
     eigenvalues H         14.11680
                eV         384.1408

        
        

**Output text.**

```xml
<comment class="example.output" id="restricted.orbitals">
      <module cmlx:lineCount="136" cmlx:templateRef="molecular.orbitals">
          <module cmlx:lineCount="5" cmlx:templateRef="orbital.line">
            <array dataType="xsd:string" size="5" dictRef="cc:irrep">1a1' 2a1' 3a1' 4a1' 5a1'</array>
            <array dataType="xsd:double" size="5" dictRef="t:eigen">-256.02776 -29.97174 -10.18645 -3.38954 -0.88456</array>
            <array dataType="xsd:double" size="5" dictRef="t:orbitalenergy">-6966.9251 -815.579 -277.1896 -92.2348 -24.0702</array>
            <array dataType="xsd:string" size="5" dictRef="cc:occupation">2.0000 2.0000 2.0000 2.0000 2.0000</array>
          </module>
          <module cmlx:lineCount="5" cmlx:templateRef="orbital.line">
            <array dataType="xsd:string" size="5" dictRef="cc:irrep">6a1' 7a1' 8a1' 9a1' 10a1'</array>
            <array dataType="xsd:double" size="5" dictRef="t:eigen">-0.5276 -0.40581 -0.22513 0.04248 0.15326</array>
            <array dataType="xsd:double" size="5" dictRef="t:orbitalenergy">-14.3569 -11.0428 -6.1262 1.1561 4.1703</array>
            <array dataType="xsd:string" size="3" dictRef="cc:occupation">2.0000 2.0000 2.0000</array>
          </module>
          <module cmlx:lineCount="3" cmlx:templateRef="orbital.line">
            <array dataType="xsd:string" size="1" dictRef="cc:irrep">21e2"</array>
            <array dataType="xsd:double" size="1" dictRef="t:eigen">14.1168</array>
            <array dataType="xsd:double" size="1" dictRef="t:orbitalenergy">384.1408</array>
          </module>      
      </module>   
    </comment>
```

## orbital.line {#orbital.line-d3e24581}


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
          <array dataType="xsd:string" size="5" dictRef="cc:occupation">2.0000 2.0000 2.0000 2.0000 2.0000</array>
      </module>
    
    
    </comment>
```
