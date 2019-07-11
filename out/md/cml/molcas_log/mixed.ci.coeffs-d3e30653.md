# mixed.ci.coeffs {#mixed.ci.coeffs-d3e30653}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | mixed.ci.coeffs                                                                                                                                     |
| name                                                                                                                                                | The CI coefficients for the MIXED states                                                                                                            |
| pattern                                                                                                                                             | \\s\*The\\sCI\\scoefficients\\sfor\\sthe\\sMIXED\\sstate.\*                                                                                         |
| endPattern                                                                                                                                          | .\*\[0-9\]{4,}\\s\*\$\\s\*                                                                                                                          |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 2                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/ci/mixed.ci.coeffs.xml                                                                                                                      |

######Template attributes

**Comment.**

      The CI coefficients for the MIXED state nr.   1
    --------------------------------------------------------------------------------
     CI COEFFICIENTS LARGER THAN  0.50D-01
      Occupation of active orbitals, and spin coupling
      of open shells. (u,d: Spin up or down).
      SGUGA info is (Midvert:IsyUp:UpperWalk/LowerWalk)
       Conf   SGUGA info Occupation       Coef       Weight
          8 ( 2:1:  1/  2)   u20uu          -0.771390         0.595043
         10 ( 2:1:  1/  4)   uduuu           0.306685         0.094056
         12 ( 2:1:  1/  6)   uuduu          -0.177065         0.031352
         13 ( 2:1:  1/  7)   u02uu           0.434433         0.188732
         16 ( 3:1:  2/  1)   uuudu          -0.237319         0.056320
         17 ( 3:1:  3/  1)   uuuud           0.185033         0.034237
     
        

**Input.**

      The CI coefficients for the MIXED state nr.   1
    --------------------------------------------------------------------------------
     CI COEFFICIENTS LARGER THAN 0.50D-01
      Occupation of active orbitals, and spin coupling
      of open shells. (u,d: Spin up or down).
       ConfOccupation       Coef       Weight                                       
      
          2    uuu0u           0.184637         0.034091
          3    uu0uu           0.369859         0.136796
          4    u0uuu          -0.716900         0.513946
          5    0uuuu          -0.561385         0.315153

        

**Output text.**

```xml
<comment class="example.output" id="ci.coeffs">
         <module cmlx:templateRef="ci.coeffs">
            <scalar dataType="xsd:integer" dictRef="m:mixedstate">1</scalar>
            <array dataType="xsd:integer" dictRef="m:configuration" size="3">2 3 4</array>
            <array dataType="xsd:string" delimiter="I" dictRef="x:value" size="3">uuu0uIuu0uuIu0uuu</array>
            <array dataType="xsd:double" dictRef="m:coeff" size="3">0.184637 0.369859 -0.716900</array>
            <array dataType="xsd:double" dictRef="m:weight" size="3">0.034091 0.136796 0.513946</array>
         </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="ci.coeffs2">
        <module cmlx:templateRef="mixed.ci.coeffs">                
            <scalar dataType="xsd:integer" dictRef="m:mixedstate">1</scalar>
            <array dataType="xsd:integer" dictRef="m:configuration" size="6">8 10 12 13 16 17</array>
            <array dataType="xsd:string" delimiter="I" dictRef="m:sguga" size="6">2:1:  1/  2I2:1:  1/  4I2:1:  1/  6I2:1:  1/  7I3:1:  2/  1I3:1:  3/  1</array>
            <array dataType="xsd:string" delimiter="I" dictRef="x:value" size="6">u20uuIuduuuIuuduuIu02uuIuuuduIuuuud</array>
            <array dataType="xsd:double" dictRef="m:coeff" size="6">-0.771390 0.306685 -0.177065 0.434433 -0.237319 0.185033</array>
            <array dataType="xsd:double" dictRef="m:weight" size="6">0.595043 0.094056 0.031352 0.188732 0.056320 0.034237</array>
         </module>
    </comment>
```
