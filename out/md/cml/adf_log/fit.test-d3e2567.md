# fit.test {#fit.test-d3e2567}

ADF log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | fit.test                                                                                                                                            |
| name                                                                                                                                                | Fit test                                                                                                                                            |
| pattern                                                                                                                                             | \\s\*Fit\\stest:.\*                                                                                                                                 |
| endPattern                                                                                                                                          | \\s\*SCF:.\*                                                                                                                                        |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | fit.test.xml                                                                                                                                        |

######Template attributes

**Input.**

     Fit test: (difference of exact and fit density, squared integrated, result summed over spins)
             Sum-of-Fragments:                             0.00000604855883
             Orthogonalized Fragments:                     0.01126932738939
             SCF:                                          0.00379056264226 
        

**Output text.**

```xml
<comment class="example.output" id="fit.test"> 
        <module cmlx:lineCount="4" cmlx:templateRef="fit.test">
            <scalar dataType="xsd:double" dictRef="cc:sumfragments">6.04855883E-6</scalar>
            <scalar dataType="xsd:double" dictRef="cc:ortho">0.01126932738939</scalar>
            <scalar dataType="xsd:double" dictRef="cc:fitscf">0.00379056264226</scalar>
        </module>
    </comment>
```
