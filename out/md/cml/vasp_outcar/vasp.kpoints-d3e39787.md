# vasp.kpoints {#vasp.kpoints-d3e39787}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Partial.png)                                                                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | VASP KPOINTS                                                                                                                                                                                          |
| id                                                                                                                                                                                                    | vasp.kpoints                                                                                                                                                                                          |
| name                                                                                                                                                                                                  | VASP KPOINTS                                                                                                                                                                                          |
| xml:base                                                                                                                                                                                              | topTemplate.xml                                                                                                                                                                                       |

######Template attributes

**Input.**

     Automatic generation mesh
     0
    Gamma
     3  3  1 
     0. 0. 0.
        

**Output text.**

```xml
<comment class="example.output" id="vasp.kpoints">
        <module id="vasp.contcar">
            <scalar dataType="xsd:string" dictRef="v:meshScheme">Gamma</scalar>
            <array dataType="xsd:integer" dictRef="v:subdivisionN" size="3">3 3 1</array>
            <array dataType="xsd:double" dictRef="v:shiftS" size="3">0. 0. 0.</array>
        </module>
    </comment>
```
