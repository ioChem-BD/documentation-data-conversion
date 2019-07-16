# jobcpu {#jobcpu-d3e17433}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Partial.png)                                                                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Gaussian log                                                                                                                                                                                          |
| id                                                                                                                                                                                                    | jobcpu                                                                                                                                                                                                |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| pattern                                                                                                                                                                                               | \\s\*Job cpu time:.\*                                                                                                                                                                                 |
| endPattern                                                                                                                                                                                            | \\s\*Normal termination.\*                                                                                                                                                                            |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | jobcpu.xml                                                                                                                                                                                            |

######Template attributes

**Input.**

     Job cpu time:  0 days  0 hours  0 minutes 12.7 seconds.
     File lengths (MBytes):  RWF=     12 Int=      0 D2E=      0 Chk=      7 Scr=      1
     Normal termination of Gaussian 03 at Mon Nov 20 14:40:36 2006.
      

**Output text.**

```xml
<comment class="example.output" id="jobcpu">
    <module cmlx:templateRef="jobcpu">
      <scalar dictRef="cc:jobtime" dataType="xsd:string">PT12.700S</scalar>
      <scalar dataType="xsd:date" dictRef="cc:jobdatetime.end">2006-11-20T14:40:36Z</scalar>
      <scalar dataType="xsd:string" dictRef="cc:program">Gaussian 03</scalar>
    </module>
  </comment>
```
