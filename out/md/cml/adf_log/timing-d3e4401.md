# timing {#timing-d3e4401}

ADF log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | ADF log                                                                                                                                                                                               |
| id                                                                                                                                                                                                    | timing                                                                                                                                                                                                |
| name                                                                                                                                                                                                  | Timing statistics resume                                                                                                                                                                              |
| pattern                                                                                                                                                                                               | \\s\*Timing\\sStatistics.\*                                                                                                                                                                           |
| endPattern                                                                                                                                                                                            | .\*\\.{5,}+(\\s+\\S+\\s\*){6}.\*\$\\s\*\$\\s\*                                                                                                                                                        |
| offset                                                                                                                                                                                                | -1                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 2                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | timing.xml                                                                                                                                                                                            |

######Template attributes

**Input.**

     =================
     Timing Statistics
     =================
      
     Total Used :                     CPU=        0.32      System=        0.16     Elapsed=        1.05
     
      Calls  Section                     ( Mean, Percentage )
     ---------------------------------------------------------------------------------------------------
         2          ................      0.00    0.00             0.00    0.00             0.00    0.00
         1  EXIT PROCEDURE .........      0.75  100.00             0.16  100.00             0.99  100.00
         
        

**Output text.**

```xml
<comment class="example.output" id="timing">
       <module cmlx:lineCount="11" cmlx:templateRef="timing">
        <scalar dataType="xsd:double" dictRef="cc:cputime">0.32</scalar>
        <scalar dataType="xsd:double" dictRef="cc:systemtime">0.16</scalar>
        <scalar dataType="xsd:double" dictRef="cc:elapsedtime">1.05</scalar>
       </module>  
    </comment>
```
