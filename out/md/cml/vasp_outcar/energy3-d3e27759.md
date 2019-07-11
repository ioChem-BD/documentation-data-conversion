# energy3 {#energy3-d3e27759}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | energy3                                                                                                                                             |
| name                                                                                                                                                | Energy section 3                                                                                                                                    |
| pattern                                                                                                                                             | \\s\*E-fermi\\s:.\*                                                                                                                                 |
| endPattern                                                                                                                                          | .\*                                                                                                                                                 |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | energy3.xml                                                                                                                                         |

######Template attributes

**Input.**

     E-fermi :  -0.1238     XC(G=0):  -6.5267     alpha+bet : -6.4535       
        

**Output text.**

```xml
<comment class="example.output" id="energy2">
        <module cmlx:templateRef="energy3" id="energy3">
            <scalar dataType="xsd:double" dictRef="v:efermi" units="nonsi:electronvolt">-0.1238</scalar>
        </module> 
    </comment>
```
