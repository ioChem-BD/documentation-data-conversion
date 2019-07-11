# preddelta {#preddelta-d3e11042}

Gaussian log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Gaussian log                                                                                                                                        |
| id                                                                                                                                                  | preddelta                                                                                                                                           |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| name                                                                                                                                                | Predicted change in Energy                                                                                                                          |
| pattern                                                                                                                                             | \\s\*Predicted change in Energy.\*                                                                                                                  |
| endPattern                                                                                                                                          | \\s\*.\*                                                                                                                                            |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| xml:base                                                                                                                                            | l103/l103.preddelta.xml                                                                                                                             |

######Template attributes

**Input.**

     Predicted change in Energy=-9.782485D-04
      

**Output text.**

```xml
<comment class="example.output" id="l103.preddelta">
    <module cmlx:templateRef="preddelta">
      <list cmlx:templateRef="predicted">
        <scalar dataType="xsd:double" dictRef="g:predchange">-9.782485E-4</scalar>
      </list>
    </module>
  </comment>
```

-   [l103.catchall](/out/md/cml/gaussian_log/l103.catchall-d3e11052.md)
