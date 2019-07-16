# parameters {#parameters-d3e979}

ADF log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | ADF log                                                                                                                                                                                               |
| id                                                                                                                                                                                                    | parameters                                                                                                                                                                                            |
| name                                                                                                                                                                                                  | Model parameters                                                                                                                                                                                      |
| pattern                                                                                                                                                                                               | \\s\*DENSITY\\sFUNCTIONAL\\sPOTENTIAL.\*                                                                                                                                                              |
| endPattern                                                                                                                                                                                            | \\s\*\$\\s\*                                                                                                                                                                                          |
| endPattern2                                                                                                                                                                                           | \\s\*SOLVATION\\s\*                                                                                                                                                                                   |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | parameters.xml                                                                                                                                                                                        |

######Template attributes

**Input.**

     DENSITY FUNCTIONAL POTENTIAL (scf)
        LDA:                               VWN                                      
        Gradient Corrections:              Becke88 Perdew86                        == Not Default ==

     SPIN  (restricted / unrestr.)
        Molecule:                          Restricted                               

     OTHER ASPECTS
        Relativistic Corrections:          scalar (ZORA,SAPA)                       *** SPECIAL ***

        Nuclear Charge Density Model:      Point Charge Nuclei                                                                                                                                                                                     
        Core Treatment:                    Frozen Orbital(s)                        

        Electric Field:                    ---                                      

        Hyperfine or Zeeman Interaction:   ---                                          

        
        

**Output text.**

```xml
<comment class="example.output" id="parameters">       
        <module cmlx:lineCount="17" cmlx:templateRef="parameters">
          <scalar id="method" dictRef="cc:method" dataType="xsd:string">DFT</scalar>
          <list cmlx:lineCount="3" cmlx:templateRef="scf">
            <scalar dataType="xsd:string" dictRef="cc:functional">VWN</scalar>
            <scalar dataType="xsd:string" dictRef="cc:functional">Becke88 Perdew86</scalar>
          </list>
          <list cmlx:lineCount="3" cmlx:templateRef="spin">
            <scalar dataType="xsd:string" dictRef="cc:spinMolecule">Restricted</scalar>
            <scalar dataType="xsd:string" dictRef="cc:spinFragments">Restricted</scalar>
          </list>
          <list cmlx:lineCount="9" cmlx:templateRef="other"> OTHER ASPECTS 
            <scalar dataType="xsd:string" dictRef="a:relcor">scalar (ZORA,SAPA)</scalar>
            <scalar dataType="xsd:string" dictRef="a:densityMode">Point Charge Nuclei</scalar>
            <scalar dataType="xsd:string" dictRef="a:coretreat">Frozen Orbital(s)</scalar>
           </list>           
        </module>
    </comment>
```
