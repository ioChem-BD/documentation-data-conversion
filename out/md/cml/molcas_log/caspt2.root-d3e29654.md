# caspt2.root {#caspt2.root-d3e29654}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | caspt2.root                                                                                                                                         |
| pattern                                                                                                                                             | \\s\*(\\+\\+)?\\s\*CASPT2\\scomputation.\*                                                                                                          |
| endPattern                                                                                                                                          | .\*                                                                                                                                                 |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/caspt2/roots.xml                                                                                                                            |

######Template attributes

**Input.**

    ++ CASPT2 computation    5
        

**Output text.**

```xml
<comment class="example.output" id="caspt2.root">
         <module cmlx:templateRef="caspt2.root">
            <list cmlx:templateRef="missingID">
               <scalar dataType="xsd:integer" dictRef="m:rootnumber">5</scalar>
            </list>
         </module>
    </comment>
```
