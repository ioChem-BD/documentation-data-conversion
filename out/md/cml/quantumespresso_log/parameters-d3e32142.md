# parameters {#parameters-d3e32142}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | QuantumEspresso log                                                                                                                                 |
| id                                                                                                                                                  | parameters                                                                                                                                          |
| name                                                                                                                                                | Calculation parameters                                                                                                                              |
| pattern                                                                                                                                             | \^\\s\*bravais-lattice\\sindex.\*                                                                                                                   |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | ./initialization/parameters.xml                                                                                                                     |

######Template attributes

**Input.**

         bravais-lattice index     =           14
         lattice parameter (alat)  =      19.3326  a.u.
         unit-cell volume          =   17343.5722 (a.u.)^3
         number of atoms/cell      =          136
         number of atomic types    =            5
         number of electrons       =      1264.00
         number of Kohn-Sham states=          758
         kinetic-energy cutoff     =      40.0000  Ry
         charge density cutoff     =     320.0000  Ry
         convergence threshold     =      1.0E-09
         mixing beta               =       0.1514
         number of iterations used =            8  plain     mixing
         Exchange-correlation      = PBE ( 1  4  3  4 0 0)
          
        

**Output text.**

```xml
<comment class="example.output" id="parameters">
        <module cmlx:templateRef="parameters">             
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">bravais-lattice index</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value">14</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">lattice parameter (alat)</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value" units="nonsi:angstrom">10.230478186</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">unit-cell volume</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value" units="nonsi:angstrom3">9368.011837611999</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">number of atoms/cell</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value">134</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">number of atomic types</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value">4</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">number of electrons</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value">1274.00</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">number of Kohn-Sham states</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value">764</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">kinetic-energy cutoff</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value" units="nonsi:electronvolt">544.22792264</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">charge density cutoff</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value" units="nonsi:electronvolt">4353.82338112</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">convergence threshold</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value" units="nonsi:angstrom">5.2918E-10</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">mixing beta</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value">0.1400</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">number of iterations used</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value">8  plain     mixing</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">Exchange-correlation</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value">PBE ( 1  4  3  4 0 0)</scalar>
         </list>
         <list>
            <scalar dataType="xsd:string" dictRef="cc:parameter">nstep</scalar>
            <scalar dataType="xsd:string" dictRef="cc:value">50</scalar>
         </list>   
        </module> 
    </comment>
```
