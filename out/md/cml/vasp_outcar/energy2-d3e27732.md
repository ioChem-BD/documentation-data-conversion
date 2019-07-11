# energy2 {#energy2-d3e27732}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | energy2                                                                                                                                             |
| name                                                                                                                                                | Energy section 2                                                                                                                                    |
| pattern                                                                                                                                             | \\s\*d\\sForce\\s=.\*                                                                                                                               |
| endPattern                                                                                                                                          | \\s\*d\\sForce.\*d\\sEwald.\*                                                                                                                       |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | energy2.xml                                                                                                                                         |

######Template attributes

**Input.**

        d Force = 0.6233654E-03[ 0.149E-02,-0.247E-03]  d Energy = 0.6368289E-03-0.135E-04
        d Force = 0.2547416E-01[ 0.255E-01, 0.255E-01]  d Ewald  = 0.2547237E-01 0.178E-05  
        

**Output text.**

```xml
<comment class="example.output" id="energy2">
        <module cmlx:lineCount="3" cmlx:templateRef="energy2">
            <scalar dataType="xsd:double" dictRef="cc:deltaEnergy" units="nonsi:electronvolt">0.0006368289</scalar>
        </module>
    </comment>
```
