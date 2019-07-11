# lowfreq {#lowfreq-d3e13868}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Gaussian log                                                                                                                                        |
| id                                                                                                                                                  | lowfreq                                                                                                                                             |
| pattern                                                                                                                                             | \\sLow frequencies.\*                                                                                                                               |
| endPattern                                                                                                                                          | .\*                                                                                                                                                 |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | l716.lowfreq.xml                                                                                                                                    |

######Template attributes

**Input.**

     Low frequencies ---    0.0018    0.0024    0.0026    6.3218    7.5564   17.5412
     Low frequencies ---   55.1764   72.8335  137.6925
      

**Output text.**

```xml
<comment class="example.output" id="l716.lowfreq">
    <module cmlx:templateRef="lowfreq">
      <array dataType="xsd:double" size="9" dictRef="g:1716.lowfreq" cmlx:templateRef="lowfreq">0.0018 0.0024 0.0026 6.3218 7.5564 17.5412 55.1764 72.8335 137.6925</array>
    </module>
  </comment>
```
