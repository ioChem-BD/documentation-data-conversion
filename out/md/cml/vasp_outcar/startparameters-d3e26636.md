# startparameters {#startparameters-d3e26636}

VASP outcar

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Partial.png)                                                                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | VASP outcar                                                                                                                                                                                           |
| id                                                                                                                                                                                                    | startparameters                                                                                                                                                                                       |
| name                                                                                                                                                                                                  | Startparameter for this run                                                                                                                                                                           |
| pattern                                                                                                                                                                                               | \\s\*Startparameter\\sfor\\sthis\\srun:\\s\*                                                                                                                                                          |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| xml:base                                                                                                                                                                                              | startparameters.xml                                                                                                                                                                                   |

######Template attributes

**Input.**

     Startparameter for this run:
       NWRITE =      2    write-flag & timer
       PREC   = normal    normal or accurate (medium, high low for compatibility)
       ISTART =      1    job   : 0-new  1-cont  2-samecut
       ICHARG =      0    charge: 1-file 2-atom 10-const
       ISPIN  =      2    spin polarized calculation?
       LNONCOLLINEAR =      F non collinear calculations
       LSORBIT =      F    spin-orbit coupling
       INIWAV =      1    electr: 0-lowe 1-rand  2-diag
       LASPH  =      T    aspherical Exc in radial PAW
       METAGGA=      F    non-selfconsistent MetaGGA calc.
        
        

**Output text.**

```xml
<comment class="example.output" id="startparameters"> 
        <module cmlx:templateRef="startparameters">
            <module>
                <list cmlx:templateRef="missingID">
                    <scalar dataType="xsd:integer" dictRef="v:ispin">2</scalar>
                </list>
            </module>
        </module> 
    </comment>
```
