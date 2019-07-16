# title {#title-d3e23525}

Turbomole log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole log                                                                                                                                                                                         |
| id                                                                                                                                                                                                    | title                                                                                                                                                                                                 |
| name                                                                                                                                                                                                  | Calculation title                                                                                                                                                                                     |
| pattern                                                                                                                                                                                               | \\s+\\\*{20,}.\*\$(?!\\s+\\\*).\*\$\\s+\\\*{20,}.\*                                                                                                                                                   |
| endPattern                                                                                                                                                                                            | \\s+\\\*{20,}.\*                                                                                                                                                                                      |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | title.xml                                                                                                                                                                                             |

######Template attributes

**Input.**

       *************************************************************************
       Fe(bipy)3 MLCT                                                           
       *************************************************************************    
        

**Output text.**

```xml
<comment class="example.output" id="title">
        <module cmlx:lineCount="3" cmlx:templateRef="title">
            <scalar dataType="xsd:string" dictRef="cc:title">Fe(bipy)3 MLCT</scalar>
        </module> 
    </comment>
```
