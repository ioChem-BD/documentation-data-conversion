# species {#species-d3e33481}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | QuantumEspresso log                                                                                                                                                                                   |
| id                                                                                                                                                                                                    | species                                                                                                                                                                                               |
| name                                                                                                                                                                                                  | Atomic species                                                                                                                                                                                        |
| pattern                                                                                                                                                                                               | \^\\s\*atomic\\s+species.\*                                                                                                                                                                           |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | ./initialization/atomic-species.xml                                                                                                                                                                   |

######Template attributes

**Input.**

         atomic species   valence    mass     pseudopotential
            Fe1           16.00    55.84500     Fe( 1.00)
            Fe2           16.00    55.84500     Fe( 1.00)
            O              6.00    15.99990     O ( 1.00)
            H              1.00     1.00790     H ( 1.00)
            
       

**Output text.**

```xml
<comment class="example.output" id="species">
    <module cmlx:templateRef="species">
        <list cmlx:templateRef="species">
            <array dataType="xsd:string" dictRef="qex:specie" size="4">Fe1 Fe2 O H</array>
            <array dataType="xsd:double" dictRef="x:valelectrons" size="4">16.00 16.00 6.00 1.00</array>
            <array dataType="xsd:double" dictRef="cc:mass" size="4">55.84500 55.84500 15.99990 1.00790</array>
            <array dataType="xsd:string" dictRef="cc:elementType" size="4">Fe Fe O H</array>
            <array dataType="xsd:double" dictRef="qex:pseudopot" size="4">1.00 1.00 1.00 1.00</array>
        </list>
        <map id="speciesToAtomTypeMap">
            <link from="Fe1" to="Fe" />
            <link from="Fe2" to="Fe" />
            <link from="O" to="O" />
            <link from="H" to="H" />
        </map>        
    </module>
   </comment>
```
