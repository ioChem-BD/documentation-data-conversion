# atoms {#atoms-d3e36090}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole control file                                                                                                                                                                                |
| id                                                                                                                                                                                                    | atoms                                                                                                                                                                                                 |
| name                                                                                                                                                                                                  | Atom definition section                                                                                                                                                                               |
| pattern                                                                                                                                                                                               | \\s\*\\u0024atoms\\s\*                                                                                                                                                                                |
| endPattern                                                                                                                                                                                            | \\s\*\\u0024.\*                                                                                                                                                                                       |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | atoms.xml                                                                                                                                                                                             |

######Template attributes

**Input.**

    $atoms
    ru 1                                                                           \
       basis =ru def2-SVP                                                          \
       ecp   =ru def2-ecp                                                          \
       jbas  =ru def2-SVP
    n  2-7                                                                         \
       basis =n def2-SVP                                                           \
       jbas  =n def2-SVP
    h  8-31                                                                        \
       basis =h def2-SVP                                                           \
       jbas  =h def2-SVP
    c  32-61                                                                       \
       basis =c def2-SVP                                                           \
       jbas  =c def2-SVP    
        

**Output text.**

```xml
<comment class="example.output" id="atoms">
       <module cmlx:templateRef="atoms">
          <module cmlx:templateRef="atomdef">
             <list dictRef="t:atom">
                <scalar dataType="xsd:string" dictRef="cc:elementType">ru</scalar>
                <scalar dataType="xsd:string" dictRef="t:atomrange">1</scalar>
             </list>
             <list dictRef="t:basis">
                <scalar dataType="xsd:string" dictRef="cc:elementType">ru</scalar>
                <scalar dataType="xsd:string" dictRef="t:basis">def2-SVP</scalar>
             </list>
             <list dictRef="t:ecp">
                <scalar dataType="xsd:string" dictRef="cc:elementType">ru</scalar>
                <scalar dataType="xsd:string" dictRef="t:ecp">def2-ecp</scalar>
             </list>
          </module>
          <module cmlx:templateRef="atomdef">
             <list dictRef="t:atom">
                <scalar dataType="xsd:string" dictRef="cc:elementType">n</scalar>
                <scalar dataType="xsd:string" dictRef="t:atomrange">2-7</scalar>
             </list>
             <list dictRef="t:basis">
                <scalar dataType="xsd:string" dictRef="cc:elementType">n</scalar>
                <scalar dataType="xsd:string" dictRef="t:basis">def2-SVP</scalar>
             </list>
          </module>
          <module cmlx:templateRef="atomdef">
             <list dictRef="t:atom">
                <scalar dataType="xsd:string" dictRef="cc:elementType">h</scalar>
                <scalar dataType="xsd:string" dictRef="t:atomrange">8-31</scalar>
             </list>
             <list dictRef="t:basis">
                <scalar dataType="xsd:string" dictRef="cc:elementType">h</scalar>
                <scalar dataType="xsd:string" dictRef="t:basis">def2-SVP</scalar>
             </list>
          </module>
          <module cmlx:templateRef="atomdef">
             <list dictRef="t:atom">
                <scalar dataType="xsd:string" dictRef="cc:elementType">c</scalar>
                <scalar dataType="xsd:string" dictRef="t:atomrange">32-61</scalar>
             </list>
             <list dictRef="t:basis">
                <scalar dataType="xsd:string" dictRef="cc:elementType">c</scalar>
                <scalar dataType="xsd:string" dictRef="t:basis">def2-SVP</scalar>
             </list>
          </module>
       </module>  
    </comment>
```
