# convergence.info {#convergence.info-d3e25992}

Turbomole log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole log                                                                                                                                       |
| id                                                                                                                                                  | convergence.info                                                                                                                                    |
| name                                                                                                                                                | Convergence information section                                                                                                                     |
| pattern                                                                                                                                             | \\s\*\\\*{10,}\\s\*\$\\s\*CONVERGENCE\\sINFORMATION.\*                                                                                              |
| endPattern                                                                                                                                          | \\s\*\\\*{10,}\\s\*                                                                                                                                 |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | minimumts/convergence.info.xml                                                                                                                      |

######Template attributes

**Input.**

          ****************************************************************** 
                              CONVERGENCE INFORMATION

                                   Converged?     Value      Criterion
                 Energy change         yes      0.0000004   0.0000010
                 RMS of displacement   yes      0.0000800   0.0005000
                 RMS of gradient       yes      0.0000092   0.0005000
                 MAX displacement      yes      0.0003920   0.0010000
                 MAX gradient          yes      0.0000313   0.0010000
          ******************************************************************                             
        

**Input.**

          ****************************************************************** 
                              CONVERGENCE INFORMATION

                                   Converged?     Value      Criterion
                 Energy change         yes      0.0000020   0.0001000
                 MAX geom. grad.       yes      0.0008366   0.0010000
          ******************************************************************                            
        

**Output text.**

```xml
<comment class="example.output" id="convergence.info">
        <module cmlx:lineCount="10" cmlx:templateRef="convergence.info">
            <list cmlx:templateRef="energyChange">
              <scalar dataType="xsd:string" dictRef="cc:converged">yes</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.0000004</scalar>
              <scalar dataType="xsd:string" dictRef="cc:criterion">0.0000010</scalar>
            </list>
            <list cmlx:templateRef="rmsDisplacement">
              <scalar dataType="xsd:string" dictRef="cc:converged">yes</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.0000800</scalar>
              <scalar dataType="xsd:string" dictRef="cc:criterion">0.0005000</scalar>
            </list>
            <list cmlx:templateRef="rmsGradient">
              <scalar dataType="xsd:string" dictRef="cc:converged">yes</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.0000092</scalar>
              <scalar dataType="xsd:string" dictRef="cc:criterion">0.0005000</scalar>
            </list>
            <list cmlx:templateRef="maxDisplacement">
              <scalar dataType="xsd:string" dictRef="cc:converged">yes</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.0003920</scalar>
              <scalar dataType="xsd:string" dictRef="cc:criterion">0.0010000</scalar>
            </list>
            <list cmlx:templateRef="maxGradient">
              <scalar dataType="xsd:string" dictRef="cc:converged">yes</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.0000313</scalar>
              <scalar dataType="xsd:string" dictRef="cc:criterion">0.0010000</scalar>
            </list>
        </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output2" id="convergence.info">
       <module cmlx:lineCount="7" cmlx:templateRef="convergence.info">
        <list cmlx:templateRef="energyChange">
         <scalar dataType="xsd:string" dictRef="cc:converged">yes</scalar>
         <scalar dataType="xsd:string" dictRef="cc:value">0.0000020</scalar>
         <scalar dataType="xsd:string" dictRef="cc:criterion">0.0001000</scalar>
        </list>
        <list cmlx:templateRef="maxGradient">
         <scalar dataType="xsd:string" dictRef="cc:converged">yes</scalar>
         <scalar dataType="xsd:string" dictRef="cc:value">0.0008366</scalar>
         <scalar dataType="xsd:string" dictRef="cc:criterion">0.0010000</scalar>
        </list>
       </module>  
    </comment>
```
