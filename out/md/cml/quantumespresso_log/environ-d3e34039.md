# environ {#environ-d3e34039}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | QuantumEspresso log                                                                                                                                 |
| id                                                                                                                                                  | environ                                                                                                                                             |
| name                                                                                                                                                | Environ module                                                                                                                                      |
| pattern                                                                                                                                             | \\s\*Environ\\sModule.\*                                                                                                                            |
| endPattern                                                                                                                                          | .\*=.\*\[a-zA-Z0-9\]+.\*\$\\s\*                                                                                                                     |
| xml:base                                                                                                                                            | ./initialization/environ.xml                                                                                                                        |

######Template attributes

**Input.**

         Environ Module
         ==============

         Please cite
             "O. Andreussi, I. Dabo and N. Marzari, J. Chem. Phys. 136, 064102 (2012);"
         in publications or presentations arising from this work.

         compensation onset threshold      =               0.1000E+00
         switching function adopted        =                     SCCS
         density limit for vacuum region   =               0.5000E-02
         density limit for bulk solvent    =               0.1000E-03
         static permittivity               =                    78.30
         epsilon calculation mode          =               electronic
         type of numerical differentiator  =            central diff.
         number of points in num. diff.    =                        2
         required accuracy                 =               0.1000E-10
         linear mixing parameter           =                     0.60
         surface tension in input (dyn/cm) =                    50.00
         surface tension in internal units =               0.6423E-04
         delta parameter for surface depth =               0.1000E-04
         external pressure in input (GPa)  =                    -0.35
         external pressure in inter. units =              -0.2379E-04
        
        

**Output text.**

```xml
<comment class="example.output" id="environ">
        <module cmlx:templateRef="environ">       
           <list cmlx:templateRef="cite">
              <scalar dataType="xsd:string" dictRef="qex:environ.citation">"O. Andreussi, I. Dabo and N. Marzari, J. Chem. Phys. 136, 064102 (2012);"</scalar>
              <scalar dataType="xsd:string" dictRef="qex:environ.citation">in publications or presentations arising from this work.</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">compensation onset threshold</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.1000E+00</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">switching function adopted</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">SCCS</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">density limit for vacuum region</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.5000E-02</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">density limit for bulk solvent</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.1000E-03</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">static permittivity</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value" units="si:k">298.87222246132</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">epsilon calculation mode</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">electronic</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">type of numerical differentiator</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">central diff.</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">number of points in num. diff.</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">2</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">required accuracy</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.1000E-10</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">linear mixing parameter</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.60</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">surface tension in input (dyn/cm)</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">50.00</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">surface tension in internal units</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.6423E-04</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">delta parameter for surface depth</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value">0.1000E-04</scalar>
           </list>
           <list>
              <scalar dataType="xsd:string" dictRef="cc:parameter">external pressure in input</scalar>
              <scalar dataType="xsd:string" dictRef="cc:value" units="nonsi:atm">-3454.231433506</scalar>
           </list>
        </module>
    </comment>
```
