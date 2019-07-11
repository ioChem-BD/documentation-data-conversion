# jobcpu {#jobcpu-d3e35603}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOPAC log                                                                                                                                           |
| id                                                                                                                                                  | jobcpu                                                                                                                                              |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| pattern                                                                                                                                             | \\s\*WALL\\-CLOCK\\sTIME.\*                                                                                                                         |
| endPattern                                                                                                                                          | \\s\*COMPUTATION\\sTIME.\*                                                                                                                          |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | jobcpu.xml                                                                                                                                          |

######Template attributes

**Input.**

              WALL-CLOCK TIME         =  6 HOURS 55 MINUTES AND 24.447 SECONDS
              COMPUTATION TIME        =  8 HOURS  3 MINUTES AND 34.471 SECONDS
        

**Output text.**

```xml
<comment class="example.output" id="jobcpu">
        <module cmlx:templateRef="jobcpu">
            <scalar dictRef="cc:wall" units="si:seconds">24924.447</scalar>
            <scalar dictRef="cc:cputime" units="si:seconds">29014.471</scalar>
         </module>
    </comment>
```
