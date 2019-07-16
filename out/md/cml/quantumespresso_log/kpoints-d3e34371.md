# kpoints {#kpoints-d3e34371}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | QuantumEspresso log                                                                                                                                                                                   |
| id                                                                                                                                                                                                    | kpoints                                                                                                                                                                                               |
| name                                                                                                                                                                                                  | kpoints                                                                                                                                                                                               |
| pattern                                                                                                                                                                                               | \^\\s+number of k points=.\*                                                                                                                                                                          |
| endPattern                                                                                                                                                                                            | \\s\*\$\\s{1,4}\\S+.\*                                                                                                                                                                                |
| endPattern2                                                                                                                                                                                           | \\s\*\$\\s\*Dense\\s\*grid.\*                                                                                                                                                                         |
| endPattern3                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | kpoints.xml                                                                                                                                                                                           |

######Template attributes

**Input.**

         number of k points=     4  gaussian smearing, width (Ry)=  0.0200
                           cart. coord. in units 2pi/alat
            k(    1) = (   0.0000000   0.0000000   0.0000000), wk =   0.2500000
            k(    2) = (   0.0000000  -0.5773503   0.0000000), wk =   0.2500000
            k(    3) = (   0.5000000  -0.2886751   0.0000000), wk =   0.2500000
            k(    4) = (  -0.5000000  -0.2886751   0.0000000), wk =   0.2500000

                           cryst. coord.
            k(    1) = (   0.0000000   0.0000000   0.0000000), wk =   0.2500000
            k(    2) = (   0.0000000  -0.5000000   0.0000000), wk =   0.2500000
            k(    3) = (   0.5000000  -0.5000000   0.0000000), wk =   0.2500000
            k(    4) = (  -0.5000000   0.0000000   0.0000000), wk =   0.2500000

         Dense  grid:  1711295 G-vectors     FFT dimensions: ( 120, 120, 320)
         
        

**Output text.**

```xml
<comment class="example.output" id="kpoints">         
        <module cmlx:templateRef="kpoints">
            <matrix cols="3" dataType="xsd:double" dictRef="qex:kpointlist.cartesian" rows="4">0.0000000 0.0000000 0.0000000 0.0000000 -0.5773503 0.0000000 0.5000000 -0.2886751 0.0000000 -0.5000000 -0.2886751 0.0000000</matrix>
            <matrix cols="3" dataType="xsd:double" dictRef="qex:kpointlist" rows="4">0.0000000 0.0000000 0.0000000 0.0000000 -0.5000000 0.0000000 0.5000000 -0.5000000 0.0000000 -0.5000000 0.0000000 0.0000000</matrix>
            <array dataType="xsd:double" dictRef="qex:kpointweight" size="4">0.2500000 0.2500000 0.2500000 0.2500000</array>
        </module>     
    </comment>
```
