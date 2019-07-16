# total.time {#total.time-d3e35992}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | MOPAC log                                                                                                                                                                                             |
| id                                                                                                                                                                                                    | total.time                                                                                                                                                                                            |
| name                                                                                                                                                                                                  | Total job time                                                                                                                                                                                        |
| pattern                                                                                                                                                                                               | \\s\*TOTAL\\sJOB\\sTIME:.\*                                                                                                                                                                           |
| endPattern                                                                                                                                                                                            | .\*                                                                                                                                                                                                   |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | time.xml                                                                                                                                                                                              |

######Template attributes

**Input.**

     TOTAL JOB TIME:         24928.18 SECONDS

        

**Output text.**

```xml
<comment class="example.output" id="total.time">
        <module cmlx:templateRef="total.time">
            <scalar dataType="xsd:double" dictRef="cc:elapsedtime" units="si:s">24928.18</scalar>
        </module>
    </comment>
```
