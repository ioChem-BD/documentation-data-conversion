# optsetup {#optsetup-d3e23271}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Orca log                                                                                                                                                                                              |
| id                                                                                                                                                                                                    | optsetup                                                                                                                                                                                              |
| name                                                                                                                                                                                                  | Optimization Coordinate Setup                                                                                                                                                                         |
| pattern                                                                                                                                                                                               | \\s\*-{20,}\$\\s\*Redundant\\sInternal\\sCoordinates.\*                                                                                                                                               |
| endPattern                                                                                                                                                                                            | \\s\*Number\\sof\\sdegrees\\sof\\sfreedom.\*                                                                                                                                                          |
| endPattern2                                                                                                                                                                                           | \\s\*\\\*{10,}.\*                                                                                                                                                                                     |
| endPattern3                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| keep                                                                                                                                                                                                  | first                                                                                                                                                                                                 |
| xml:base                                                                                                                                                                                              | optsetup.xml                                                                                                                                                                                          |

######Template attributes

**Input.**

        -----------------------------------------------------------------
                        Redundant Internal Coordinates


        -----------------------------------------------------------------
             Definition                    Initial Value    Approx d2E/dq
        -----------------------------------------------------------------
          1. B(H   1,O   0)                  1.0000         0.448900   
          2. B(H   2,O   0)                  1.0000         0.448900   
          3. A(H   1,O   0,H   2)           90.0000         0.306850 C 
        -----------------------------------------------------------------

    Number of atoms                         .... 3
    Number of degrees of freedom            .... 3  
        

**Output text.**

```xml
<comment class="example.output" id="optsetup">        
        <module cmlx:templateRef="optsetup" dictRef="cc:userDefinedModule">
           <list>
              <scalar dataType="xsd:string" dictRef="x:restriction">A</scalar>
              <array dataType="xsd:integer" dictRef="x:serial" size="3">1 0 2</array>
              <scalar dataType="xsd:double" dictRef="x:parameter">90.0000</scalar>
              <scalar dataType="xsd:double" dictRef="o:d2E_dq">0.306850</scalar>
           </list>
        </module>
    </comment>
```
