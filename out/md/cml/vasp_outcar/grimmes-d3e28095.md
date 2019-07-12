# grimmes {#grimmes-d3e28095}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | grimmes                                                                                                                                             |
| name                                                                                                                                                | Parameters for Grimme's potential                                                                                                                   |
| pattern                                                                                                                                             | \\s\*Parameters\\sfor\\sGrimme\\'s\\spotential:.\*                                                                                                  |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | grimmes.xml                                                                                                                                         |

######Template attributes

**Input.**

      Parameters for Grimme's potential:
             C6(Jnm^6/mol)     R0(A)
       -----------------------------
       Cu       2.740          1.562
       C        1.750          1.452
       H        0.140          1.001
       O        0.700          1.342

        

**Output text.**

```xml
<comment class="example.output" id="grimmes">
        <module cmlx:templateRef="grimmes">
            <array dataType="xsd:string" dictRef="cc:elementType" size="4">Cu C H O</array>
            <array dataType="xsd:double" dictRef="v:grimmeC6" size="4">2.740 1.750 0.140 0.700</array>
            <array dataType="xsd:double" dictRef="v:grimmeR0" size="4">1.562 1.452 1.001 1.342</array>
        </module>
    </comment>
```
