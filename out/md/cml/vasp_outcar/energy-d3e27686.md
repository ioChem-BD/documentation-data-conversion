# energy {#energy-d3e27686}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | energy                                                                                                                                              |
| name                                                                                                                                                | Energy section                                                                                                                                      |
| pattern                                                                                                                                             | \\s\*FREE\\sENERGIE\\sOF\\sTHE\\sION-ELECTRON\\sSYSTEM\\s\\(eV\\).\*                                                                                |
| endPattern                                                                                                                                          | \\s\*energy\\s\*without\\sentropy.\*                                                                                                                |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | energy.xml                                                                                                                                          |

######Template attributes

**Input.**

      FREE ENERGIE OF THE ION-ELECTRON SYSTEM (eV)
      ---------------------------------------------------
      free  energy   TOTEN  =      -566.22302844 eV

      energy  without entropy=     -566.22206374  energy(sigma->0) =     -566.22254609               
        

**Output text.**

```xml
<comment class="example.output" id="energy">
        <module cmlx:templateRef="energies">
            <scalar dataType="xsd:double" dictRef="cc:freeEnergy" units="nonsi:electronvolt">-566.22302844</scalar>
            <scalar dataType="xsd:double" dictRef="v:noEntropyEnergy" units="nonsi:electronvolt">-566.22206374</scalar>
            <scalar dataType="xsd:double" dictRef="cc:e0" units="nonsi:electronvolt">-566.22254609</scalar>
        </module>
    </comment>
```
