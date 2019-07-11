# dipole {#dipole-d3e20920}

Orca log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | dipole                                                                                                                                              |
| name                                                                                                                                                | Dipole moment                                                                                                                                       |
| pattern                                                                                                                                             | \\s\*-+\\s\*\$\\s\*DIPOLE\\sMOMENT\\s\*\$\\s\*-+\\s\*                                                                                               |
| endPattern                                                                                                                                          | \\s\*Magnitude.\*\$\\s\*                                                                                                                            |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | dipole.xml                                                                                                                                          |

######Template attributes

**Input.**

    -------------
    DIPOLE MOMENT
    -------------
                                    X             Y             Z
    Electronic contribution:     -2.73052      -4.20537       0.24659
    Nuclear contribution   :      3.48724       4.50131      -0.28886
                            -----------------------------------------
    Total Dipole Moment    :      0.75672       0.29593      -0.04226
                            -----------------------------------------
    Magnitude (a.u.)       :      0.81363
    Magnitude (Debye)      :      2.06808

        

**Output text.**

```xml
<comment class="example.output" id="dipole">
        <module cmlx:templateRef="dipole">
          <array dataType="xsd:double" dictRef="cc:dipole" size="9">3.48724 -2.73052 0.75672 4.50131 -4.20537 0.29593 -0.28886 0.24659 -0.04226</array>
          <scalar dataType="xsd:double" dictRef="o:magnitude" units="nonsi2:au">0.81363</scalar>
          <scalar dataType="xsd:double" dictRef="o:magnitude" units="nonsi2:debye">2.06808</scalar>
       </module>  
    </comment>
```
