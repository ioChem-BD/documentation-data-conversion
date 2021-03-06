# pseudopotential {#pseudopotential-d3e33929}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | QuantumEspresso log                                                                                                                                                                                   |
| id                                                                                                                                                                                                    | pseudopotential                                                                                                                                                                                       |
| name                                                                                                                                                                                                  | Pseudopotential section                                                                                                                                                                               |
| pattern                                                                                                                                                                                               | \\s\*PseudoPot.\*for.\*read\\sfrom\\sfile:.\*                                                                                                                                                         |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | ./initialization/pseudopotential.xml                                                                                                                                                                  |

######Template attributes

**Input.**

         PseudoPot. # 1 for Fe read from file:
         /home/hnguyen/espresso_pseudo/Fe.pbe-sp-van_ak.UPF
         MD5 check sum: 874d5528bf087cea5d785f7b6a7bf583
         Pseudo is Ultrasoft, Zval = 16.0
         Generated by new atomic code, or converted to UPF format
         Using radial grid of  861 points,  6 beta functions with: 
                    l(1) =   0
                    l(2) =   0
                    l(3) =   1
                    l(4) =   1
                    l(5) =   2
                    l(6) =   2
         Q(r) pseudized with  8 coefficients,  rinner =    1.500   1.500   1.500
                                                           1.500   1.500
                                                            
        

**Output text.**

```xml
<comment class="example.output" id="pseudopotential">
        <module cmlx:templateRef="pseudopotential">
            <scalar dataType="xsd:integer" dictRef="cc:serial">1</scalar>
            <scalar dataType="xsd:string" dictRef="cc:elementType">Fe</scalar>
            <scalar dataType="xsd:string" dictRef="qex:pseudofile">Fe.pbe-sp-van_ak.UPF</scalar>
            <scalar dataType="xsd:string" dictRef="qex:md5sum">874d5528bf087cea5d785f7b6a7bf583</scalar>
            <scalar dataType="xsd:string" dictRef="qex:pseudopotential">Ultrasoft</scalar>
            <scalar dataType="xsd:double" dictRef="qex:zval">16.0</scalar>
            <scalar dataType="xsd:integer" dictRef="qex:gridpoints">861</scalar>
            <scalar dataType="xsd:integer" dictRef="qex:betafunctions">6</scalar>
            <list cmlx:templateRef="lvalue">
               <array dataType="xsd:integer" dictRef="cc:serial" size="6">1 2 3 4 5 6</array>
               <array dataType="xsd:integer" dictRef="cc:value" size="6">0 0 1 1 2 2</array>
            </list>
            <scalar dataType="xsd:integer" dictRef="qex:qrcoeffs">8</scalar>
            <array dataType="xsd:double" dictRef="qex:rinner" size="5">1.500 1.500 1.500 1.500 1.500</array>
         </module>
    </comment>
```
