# lattice {#lattice-d3e32322}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | QuantumEspresso log                                                                                                                                 |
| id                                                                                                                                                  | lattice                                                                                                                                             |
| name                                                                                                                                                | Lattice                                                                                                                                             |
| pattern                                                                                                                                             | \^\\s\*celldm.\*                                                                                                                                    |
| endPattern                                                                                                                                          | \\s\*b\\(3\\).\*                                                                                                                                    |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | ./initialization/lattice.xml                                                                                                                        |

######Template attributes

**Input.**

         celldm(1)=  19.332654  celldm(2)=   1.000000  celldm(3)=   2.829039
         celldm(4)=   0.000000  celldm(5)=   0.000000  celldm(6)=  -0.500000

         crystal axes: (cart. coord. in units of alat)
                   a(1) = (   1.000000   0.000000   0.000000 )  
                   a(2) = (  -0.500000   0.866025   0.000000 )  
                   a(3) = (   0.000000   0.000000   2.829039 )  

         reciprocal axes: (cart. coord. in units 2 pi/alat)
                   b(1) = (  1.000000  0.577350  0.000000 )  
                   b(2) = (  0.000000  1.154701  0.000000 )  
                   b(3) = (  0.000000  0.000000  0.353477 )        
        

**Output text.**

```xml
<comment class="example.output" id="lattice">
        <module cmlx:templateRef="lattice">                    
             <array dataType="xsd:string" dictRef="cc:lattice" size="3" units="nonsi:angstrom">10.230478 0.000000 0.000000</array>
             <array dataType="xsd:string" dictRef="cc:lattice" size="3" units="nonsi:angstrom">-5.115239 8.859850 0.000000</array>
             <array dataType="xsd:string" dictRef="cc:lattice" size="3" units="nonsi:angstrom">0.000000 0.000000 28.942422</array>       
       </module>
    </comment>
```
