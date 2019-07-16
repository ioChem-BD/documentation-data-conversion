# nuclear.repulsion {#nuclear.repulsion-d3e26143}

Turbomole log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole log                                                                                                                                                                                         |
| id                                                                                                                                                                                                    | nuclear.repulsion                                                                                                                                                                                     |
| name                                                                                                                                                                                                  | Nuclear repulsion energies                                                                                                                                                                            |
| pattern                                                                                                                                                                                               | \\s\*nuclear\\srepulsion\\senergy.\*\$\\s\*empirical.\*                                                                                                                                               |
| endPattern                                                                                                                                                                                            | \\s\*nuclear\\srepulsion\\s\\+\\sdispersion\\scorrection.\*                                                                                                                                           |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | nuclear.repulsion.xml                                                                                                                                                                                 |

######Template attributes

**Input.**

     nuclear repulsion energy                  =    4406.824720361
     empirical dispersive energy correction    =      -0.055658060
     nuclear repulsion + dispersion correction =    4406.769062301 
        

**Output text.**

```xml
<comment class="example.output" id="nuclear.repulsion">   
        <module cmlx:templateRef="nuclear.repulsion">
            <scalar dataType="xsd:double" dictRef="cc:nucrepener" units="nonsi:hartree">4406.82472036</scalar>
            <scalar dataType="xsd:double" dictRef="t:empdispcorrection" units="nonsi:hartree">-0.055658060</scalar>
        </module>
    </comment>
```
