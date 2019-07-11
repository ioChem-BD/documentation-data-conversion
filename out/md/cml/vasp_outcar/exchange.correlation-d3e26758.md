# exchange.correlation {#exchange.correlation-d3e26758}

VASP outcar


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | exchange.correlation                                                                                                                                |
| name                                                                                                                                                | Exchange correlation treatment                                                                                                                      |
| pattern                                                                                                                                             | \\s\*Exchange\\scorrelation\\streatment:\\s\*                                                                                                       |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| xml:base                                                                                                                                            | exchange.correlation.xml                                                                                                                            |

######Template attributes

**Input.**

     Exchange correlation treatment:
       GGA     =    PE    GGA type
       LEXCH   =     8    internal setting for exchange type
       VOSKOWN=      0    Vosko Wilk Nusair interpolation
       LHFCALC =     F    Hartree Fock is set to
       LHFONE  =     F    Hartree Fock one center treatment
       AEXX    =    0.0000 exact exchange contribution
        
        

**Output text.**

```xml
<comment class="example.output" id="exchange.correlation">
        <module cmlx:templateRef="exchange.correlation">  
            <module>
               <list cmlx:templateRef="missingID">
                  <scalar dataType="xsd:string" dictRef="v:gga">PE</scalar>
               </list>
            </module>
            <module cmlx:templateRef="parameter">
               <list cmlx:templateRef="missingID">
                  <list>
                     <scalar dataType="xsd:string" dictRef="v:lexch">8</scalar>
                  </list>
               </list>
            </module>
            <module cmlx:templateRef="parameter">
               <list cmlx:templateRef="missingID">
                  <list>
                     <scalar dataType="xsd:string" dictRef="v:voskown">0</scalar>
                  </list>
               </list>
            </module>
            <module cmlx:templateRef="LHFCALC">
               <list cmlx:templateRef="missingID">
                  <scalar dataType="xsd:boolean" dictRef="v:lhfcalc">false</scalar>
               </list>
            </module>
            <module cmlx:templateRef="parameter">
               <list cmlx:templateRef="missingID">
                  <list>
                     <scalar dataType="xsd:string" dictRef="v:lhfone">F</scalar>
                  </list>
               </list>
            </module>
            <module cmlx:templateRef="AEXX">
               <list cmlx:templateRef="missingID">
                  <scalar dataType="xsd:double" dictRef="v:aexx">0.0000</scalar>
               </list>
            </module>
         </module>
    </comment>
```
