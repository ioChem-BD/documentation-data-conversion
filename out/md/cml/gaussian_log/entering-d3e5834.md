# entering {#entering-d3e5834}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Gaussian log                                                                                                                                        |
| id                                                                                                                                                  | entering                                                                                                                                            |
| pattern                                                                                                                                             | \\s\*Entering Gaussian System.\*Link\\s\*0=.\*                                                                                                      |
| endPattern                                                                                                                                          | .\*Initial command\\:.\*\$.\*                                                                                                                       |
| endOffset                                                                                                                                           | 2                                                                                                                                                   |
| xml:base                                                                                                                                            | l0.entering.xml                                                                                                                                     |

######Template attributes

**Input.**

     Entering Gaussian System, Link 0=/usr/local/gaussian/g03/g03
     Initial command:
     /usr/local/gaussian/g03/l1.exe /tmp/webmo/1/Gau-28330.inp -scrdir=/tmp/webmo/1/
      

**Output text.**

```xml
<comment class="example.output" id="entering">
    <module cmlx:templateRef="entering">
      <scalar dataType="xsd:string" dictRef="g:link0">/usr/local/gaussian/g03/g03</scalar>
      <array dataType="xsd:string" size="3" dictRef="g:command">/usr/local/gaussian/g03/l1.exe /tmp/webmo/1/Gau-28330.inp -scrdir=/tmp/webmo/1/</array>
    </module>
  </comment>
```
