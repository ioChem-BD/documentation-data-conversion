# dipole {#dipole-d3e26932}

VASP outcar

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Partial.png)                                                                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | VASP outcar                                                                                                                                                                                           |
| id                                                                                                                                                                                                    | dipole                                                                                                                                                                                                |
| name                                                                                                                                                                                                  | Dipole corrections                                                                                                                                                                                    |
| pattern                                                                                                                                                                                               | \\s\*Dipole\\scorrections.\*                                                                                                                                                                          |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | dipole.xml                                                                                                                                                                                            |

######Template attributes

**Input.**

     Dipole corrections
       LMONO  =      F    monopole corrections only (constant potential shift)
       LDIPOL =      T    correct potential (dipole corrections)
       IDIPOL =      3    1-x, 2-y, 3-z, 4-all directions 
       EPSILON=  1.0000000 bulk dielectric constant
        
        

**Output text.**

```xml
<comment class="example.output" id="dipole">
        <module cmlx:templateRef="dipole">
            <module>
                <list cmlx:templateRef="missingID">
                    <scalar dataType="xsd:string" dictRef="v:ldipol">T</scalar>
                </list>
            </module>
            <module>
                <list cmlx:templateRef="missingID">
                    <scalar dataType="xsd:integer" dictRef="v:idipol">3</scalar>
                </list>
            </module>
        </module>
    </comment>
```
