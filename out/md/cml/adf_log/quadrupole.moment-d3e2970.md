# quadrupole.moment {#quadrupole.moment-d3e2970}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | ADF log                                                                                                                                                                                               |
| id                                                                                                                                                                                                    | quadrupole.moment                                                                                                                                                                                     |
| pattern                                                                                                                                                                                               | \\s\*Quadrupole Moment.\*                                                                                                                                                                             |
| endPattern                                                                                                                                                                                            | \\s\*This molecular quadrupole moment.\*                                                                                                                                                              |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | quadrupole.moment.xml                                                                                                                                                                                 |

######Template attributes

**Input.**

     Quadrupole Moment (Buckingham convention)  ***  (a.u.)  ***
     =========================================
         quad-xx        quad-xy        quad-xz        quad-yy        quad-yz        quad-zz
         54.58446200     0.00000000     0.00000000    54.58446200     0.00000000  -109.16892399

     This molecular quadrupole moment is calculated with analytic integration   
        

**Output text.**

```xml
<comment class="example.output" id="quadrupole.moment">
        <module cmlx:lineCount="7" cmlx:templateRef="quadrupole.moment">
            <array dataType="xsd:double" size="6" dictRef="cc:quadrupole">54.584462 0.0 0.0 54.584462 0.0 -109.16892399</array>
        </module>
    </comment>
```
