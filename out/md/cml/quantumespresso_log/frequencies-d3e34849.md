# frequencies {#frequencies-d3e34849}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | QuantumEspresso log                                                                                                                                                                                   |
| id                                                                                                                                                                                                    | frequencies                                                                                                                                                                                           |
| name                                                                                                                                                                                                  | Frequencies                                                                                                                                                                                           |
| pattern                                                                                                                                                                                               | \\s\*\\\*{10,}\\s\*\$\\s\*freq\\s\\(.\*                                                                                                                                                               |
| endPattern                                                                                                                                                                                            | \\s\*\\\*{10,}                                                                                                                                                                                        |
| xml:base                                                                                                                                                                                              | ./postprocessings/phonom.xml                                                                                                                                                                          |

######Template attributes

**Input.**

     **************************************************************************
         freq (    1) =      -3.022679 [THz] =    -100.825730 [cm-1]
         freq (    2) =      -1.252407 [THz] =     -41.775805 [cm-1]
         freq (    3) =       0.801352 [THz] =      26.730212 [cm-1]
         freq (    4) =       2.015948 [THz] =      67.244786 [cm-1]
         freq (    5) =       3.401824 [THz] =     113.472642 [cm-1]
         freq (    6) =     129.087361 [THz] =    4305.890869 [cm-1]
     ************************************************************************** 
        

**Output text.**

```xml
<comment class="example.output" id="frequencies">
      <module cmlx:templateRef="frequencies">
         <array dataType="xsd:string" dictRef="cc:serial" size="6">1 2 3 4 5 6</array>
         <array dataType="xsd:double" dictRef="cc:frequency" size="6" units="nonsi:cm-1">-100.825730 -41.775805 26.730212 67.244786 113.472642 4305.890869</array>
      </module>
    </comment>
```
