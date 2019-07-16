# thermochemistry {#thermochemistry-d3e19652}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Orca log                                                                                                                                                                                              |
| id                                                                                                                                                                                                    | thermochemistry                                                                                                                                                                                       |
| name                                                                                                                                                                                                  | Thermochemistry section                                                                                                                                                                               |
| pattern                                                                                                                                                                                               | \\s\*\\-+\\s\*\$\\s\*THERMOCHEMISTRY.\*\$\\s\*\\-+\\s\*                                                                                                                                               |
| endPattern                                                                                                                                                                                            | \\s\*\$\\s\*                                                                                                                                                                                          |
| endPattern2                                                                                                                                                                                           | \\s\*freq.\*\$\\s\*                                                                                                                                                                                   |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | thermochemistry.xml                                                                                                                                                                                   |

######Template attributes

**Input.**

    --------------------------
    THERMOCHEMISTRY AT 298.15K
    --------------------------

    Temperature         ... 298.15 K
    Pressure            ... 1.00 atm
    Total Mass          ... 248.32 AMU

    Throughout the following assumptions are being made:
      (1) The electronic state is orbitally nondegenerate
      (2) There are no thermally accessible electronically excited states
      (3) Hindered rotations indicated by low frequency modes) are not
          treated as such but are treated as vibrations and this may
          case some error
      (4) All equations used are the standard statistical mechanics
          equations for an ideal gas
      (5) All vibrations are strinctly harmonic


        

**Output text.**

```xml
<comment class="example.output" id="thermochemistry">
      <module cmlx:templateRef="thermochemistry">
         <scalar dataType="xsd:double" dictRef="cc:temp" units="si:k">298.15</scalar>
         <scalar dataType="xsd:double" dictRef="cc:press" units="nonsi:atm">1.00</scalar>
         <scalar dataType="xsd:double" dictRef="cc:totalmass">248.32</scalar>
      </module>
    </comment>
```
