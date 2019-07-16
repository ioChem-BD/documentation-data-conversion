# zero.point.energy {#zero.point.energy-d3e26276}

Turbomole log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole log                                                                                                                                                                                         |
| id                                                                                                                                                                                                    | zero.point.energy                                                                                                                                                                                     |
| name                                                                                                                                                                                                  | Zero point vibration energy                                                                                                                                                                           |
| pattern                                                                                                                                                                                               | \\s\*\\\*{20,}\\s\*\$\\s\*\\\*.\*\$\\s\*\\\*\\s+zero\\spoint\\sVIBRATIONAL\\senergy.\*                                                                                                                |
| endPattern                                                                                                                                                                                            | \\s\*\\\*{20,}\\s\*                                                                                                                                                                                   |
| xml:base                                                                                                                                                                                              | zero.point.energy.xml                                                                                                                                                                                 |

######Template attributes

**Input.**

          **************************************************************
          *                                                            *
          *  zero point VIBRATIONAL energy  :      0.0598644  Hartree  *
          *    SCF-energy                   :   -228.9336374           *
          *    SCF + E(vib0)                :   -228.8737730           *
          *                                                            *
          **************************************************************
        

**Output text.**

```xml
<comment class="example.output" id="zero.point.energy">
        <module cmlx:templateRef="zero.point.energy">
            <scalar dataType="xsd:double" dictRef="t:zeropoint" units="nonsi:hartree">0.0598644</scalar>
        </module> 
    </comment>
```
