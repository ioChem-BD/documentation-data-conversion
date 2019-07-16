# methods {#methods-d3e36250}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole control file                                                                                                                                                                                |
| id                                                                                                                                                                                                    | methods                                                                                                                                                                                               |
| name                                                                                                                                                                                                  | Method section                                                                                                                                                                                        |
| pattern                                                                                                                                                                                               | \\s\*\\u0024(?i:(dftIuhf))\\s\*                                                                                                                                                                       |
| endPattern                                                                                                                                                                                            | \\s\*\\u0024.\*                                                                                                                                                                                       |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | methods.xml                                                                                                                                                                                           |

######Template attributes

**Input.**

    $dft
     functional pbe0
     gridsize   6
     weight derivatives 
        

**Output text.**

```xml
<comment class="example.output" id="methods">
        <module cmlx:lineCount="4" cmlx:templateRef="methods">
            <scalar dataType="xsd:string" dictRef="cc:method">dft</scalar>
            <scalar dataType="xsd:string" dictRef="cc:functional">pbe0</scalar>
        </module>
    </comment>
```
