# constraint {#constraint-d3e31503}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | constraint                                                                                                                                          |
| name                                                                                                                                                | Contraints section                                                                                                                                  |
| pattern                                                                                                                                             | \\s\*(?i)()(CONSTRAINTS){5,}.\*                                                                                                                     |
| endPattern                                                                                                                                          | \\s\*(?i)()(CONSTRAINTS){5,}.\*\$\\s\*(?i)()(CONSTRAINTS){5,}.\*                                                                                    |
| endOffset                                                                                                                                           | 2                                                                                                                                                   |
| xml:base                                                                                                                                            | modules/constraint.xml                                                                                                                              |

######Template attributes

**Input.**

    ConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraints
    ConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraints
    Constraints                                                                                        Constraints
    Constraints                                 C O N S T R A I N T S                                  Constraints
    Constraints                                                                                        Constraints

    ************************************************************************************************************************
    A = ANGLE H1 O H2                                                                                                       
    VALUES                                                                                                                  
    A = 110 DEGREES                                                                                                         
    ************************************************************************************************************************


     *************************************************************
     * Values of the primitive constraints                       *
     *************************************************************
     A        : Angle=      108.9246   / Degree    1.901094 / rad


     *******************************************
     * Values of the constraints   / au or rad *
     *******************************************
       Label        C         C0
     Cns001      1.901094  1.919862

    Constraints                                                                                        Constraints
    ConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraints
    ConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraintsConstraints          
        

**Output text.**

```xml
<comment class="example.output" id="constraint">
        <module cmlx:templateRef="constraint">
            <list>
               <scalar dataType="xsd:string" dictRef="m:restrictionlabel">A</scalar>
               <scalar dataType="xsd:string" dictRef="m:restriction">ANGLE</scalar>
               <scalar dataType="xsd:string" dictRef="m:restrictionextras">H1 O H2</scalar>
            </list>
            <list>
               <scalar dataType="xsd:string" dictRef="m:restrictionlabel">A</scalar>
               <scalar dataType="xsd:string" dictRef="m:restrictionvalue">110</scalar>
               <scalar dataType="xsd:string" dictRef="m:restrictionunit">DEGREES</scalar>
            </list>
         </module>
    </comment>
```
