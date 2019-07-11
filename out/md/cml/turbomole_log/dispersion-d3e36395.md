# dispersion {#dispersion-d3e36395}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole control file                                                                                                                              |
| id                                                                                                                                                  | dispersion                                                                                                                                          |
| name                                                                                                                                                | Empirical dispersion correction                                                                                                                     |
| pattern                                                                                                                                             | \\s\*\\u0024\\s\*(?i:(disp3IolddispIdisp))\\s\*                                                                                                     |
| endPattern                                                                                                                                          | .\*                                                                                                                                                 |
| xml:base                                                                                                                                            | dispersion.xml                                                                                                                                      |

######Template attributes

**Input.**

    $disp3      
        

**Output text.**

```xml
<comment class="example.output" id="dispersion">
        <module cmlx:templateRef="dispersion">
            <scalar dataType="xsd:string" dictRef="t:correction">disp3</scalar>
        </module>     
    </comment>
```
