# quadrupole {#quadrupole-d3e20987}

Orca log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | quadrupole                                                                                                                                          |
| name                                                                                                                                                | Quadrupole moment                                                                                                                                   |
| pattern                                                                                                                                             | \\s\*-{20,}\\s\*\$\\s\*QUADRUPOLE\\sMOMENT.\*                                                                                                       |
| endPattern                                                                                                                                          | \\s\*TOT                                                                                                                                            |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | quadrupole.xml                                                                                                                                      |

######Template attributes

**Input.**

    ------------------------
    QUADRUPOLE MOMENT (A.U.)
    ------------------------

                    XX           YY           ZZ           XY           XZ           YZ
      NUC       309.71894    532.88655      1.56654    194.61613    -18.36476    -25.54123
      EL       -336.59758   -568.46250    -37.10241   -194.83123     18.01215     25.52800
      TOT       -26.87864    -35.57595    -35.53587     -0.21510     -0.35261     -0.01323
        

**Output text.**

```xml
<comment class="example.output" id="quadrupole">
        <module cmlx:templateRef="quadrupole">
            <array dataType="xsd:double" dictRef="cc:quadrupole" size="18">309.71894 -336.59758 -26.87864 532.88655 -568.46250 -35.57595 1.56654 -37.10241 -35.53587 194.61613 -194.83123 -0.21510 -18.36476 18.01215 -0.35261 -25.54123 25.52800 -0.01323</array>
        </module>
    </comment>
```
