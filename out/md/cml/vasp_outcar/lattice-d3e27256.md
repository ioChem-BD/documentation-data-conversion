# lattice {#lattice-d3e27256}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | lattice                                                                                                                                             |
| name                                                                                                                                                | Lattice vectors                                                                                                                                     |
| pattern                                                                                                                                             | \\s\*direct\\slattice\\svectors\\s\*reciprocal\\slattice\\svectors.\*                                                                               |
| endPattern                                                                                                                                          | \\s\*\\w+.\*\$\\s\*                                                                                                                                 |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | position/lattice.xml                                                                                                                                |

######Template attributes

**Input.**

          direct lattice vectors                 reciprocal lattice vectors
        13.011000000  0.000000000  0.000000000     0.076858043  0.000000000  0.000000000
         0.000000000 13.011000000  0.000000000     0.000000000  0.076858043  0.000000000
         0.000000000  0.000000000 19.337000000     0.000000000  0.000000000  0.051714330
        
        

**Output text.**

```xml
<comment class="example.output" id="lattice">
        <module cmlx:templateRef="lattice">
            <array dataType="xsd:double" dictRef="cc:lattice" size="3">13.011000000 0.000000000 0.000000000</array>
            <array dataType="xsd:double" dictRef="cc:lattice" size="3">0.000000000 13.011000000 0.000000000</array>
            <array dataType="xsd:double" dictRef="cc:lattice" size="3">0.000000000 0.000000000 19.337000000</array>
        </module> 
    </comment>
```
