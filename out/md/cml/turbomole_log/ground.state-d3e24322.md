# ground.state {#ground.state-d3e24322}

Turbomole log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole log                                                                                                                                       |
| id                                                                                                                                                  | ground.state                                                                                                                                        |
| name                                                                                                                                                | Ground state                                                                                                                                        |
| pattern                                                                                                                                             | \\s\*Ground\\sstate.\*                                                                                                                              |
| endPattern                                                                                                                                          | \\sTotal\\senergy.\*                                                                                                                                |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | ground.state.xml                                                                                                                                    |

######Template attributes

**Input.**

                                    Ground state


     Total energy:                           -2746.335418094000 
        

**Output text.**

```xml
<comment class="example.output" id="ground.state">
        <module cmlx:lineCount="4" cmlx:templateRef="ground.state">
            <scalar dataType="xsd:double" dictRef="t:groundenergy">-2746.335418094</scalar>
        </module> 
    </comment>
```
