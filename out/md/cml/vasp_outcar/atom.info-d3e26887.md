# atom.info {#atom.info-d3e26887}

VASP outcar

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | VASP outcar                                                                                                                                                                                           |
| id                                                                                                                                                                                                    | atom.info                                                                                                                                                                                             |
| name                                                                                                                                                                                                  | Atom additional information                                                                                                                                                                           |
| pattern                                                                                                                                                                                               | \\s+Mass\\sof\\sIons\\sin\\sam.\*                                                                                                                                                                     |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| endPattern2                                                                                                                                                                                           | \\s\*Atomic\\sWigner-Seitz\\sradii.\*                                                                                                                                                                 |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | atom.info.xml                                                                                                                                                                                         |

######Template attributes

**Output text.**

```xml
<comment class="example,output" id="atom.info">
  Mass of Ions in am
   POMASS = 140.12 16.00 12.01  1.00
  Ionic Valenz
   ZVAL   =  12.00  6.00  4.00  1.00
  Atomic Wigner-Seitz radii
 </comment>
```

**Output text.**

```xml
<comment class="example.output" id="atom.info">
        <module cmlx:templateRef="atom.info">
            <list cmlx:templateRef="missingID">
                <list />  
            </list>
            <list cmlx:templateRef="missingID">
                <array dataType="xsd:double" dictRef="cc:mass" size="4">47.88 16.00 12.01 1.00</array>
            </list>
            <list cmlx:templateRef="missingID">
                <list />
            </list>
            <list cmlx:templateRef="missingID">
                <array dataType="xsd:double" dictRef="cc:valence" size="4">10.00 6.00 4.00 1.00</array>
            </list>
        </module>    
    </comment>
```
