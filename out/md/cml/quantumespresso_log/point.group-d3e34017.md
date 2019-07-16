# point.group {#point.group-d3e34017}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | QuantumEspresso log                                                                                                                                                                                   |
| id                                                                                                                                                                                                    | point.group                                                                                                                                                                                           |
| name                                                                                                                                                                                                  | Point group                                                                                                                                                                                           |
| pattern                                                                                                                                                                                               | \^\\s\*point\\sgroup.\*                                                                                                                                                                               |
| endPattern                                                                                                                                                                                            | .\*                                                                                                                                                                                                   |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | ./initialization/point.group.xml                                                                                                                                                                      |

######Template attributes

**Input.**

         point group C_1 (1)    
        

**Output text.**

```xml
<comment class="example.output" id="point.group">
        <module cmlx:templateRef="point.group">
            <scalar dataType="xsd:string" dictRef="cc:pointgroup">C_1 (1)</scalar>
        </module>
    </comment>
```
