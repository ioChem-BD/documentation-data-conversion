# zeropoint {#zeropoint-d3e3778}

ADF log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | zeropoint                                                                                                                                           |
| name                                                                                                                                                | Zero-point energy                                                                                                                                   |
| pattern                                                                                                                                             | \\s\*Zero-Point\\sEnergy.\*                                                                                                                         |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | zeropoint.xml                                                                                                                                       |

######Template attributes

**Input.**

     Zero-Point Energy :      0.500175 a.u.
     ===================     13.610451 eV
     (imaginary frequencies were excluded from the summation) 
        

**Output text.**

```xml
<comment class="example.output" id="zeropoint"> 
        <module cmlx:lineCount="3" cmlx:templateRef="zeropoint">
            <scalar dataType="xsd:double" dictRef="cc:zeropoint" units="nonsi:electronvolt">13.610451</scalar> 
        </module>
    </comment>
```
