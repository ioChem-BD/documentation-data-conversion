# basisecp {#basisecp-d3e21156}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Orca log                                                                                                                                                                                              |
| id                                                                                                                                                                                                    | basisecp                                                                                                                                                                                              |
| name                                                                                                                                                                                                  | ECP Parameter Information                                                                                                                                                                             |
| pattern                                                                                                                                                                                               | \\s\*-{20}.\*\$\\s\*ECP\\sPARAMETER\\sINFORMATION.\*                                                                                                                                                  |
| endPattern                                                                                                                                                                                            | \\s\*Atom.\*\$\\s\*                                                                                                                                                                                   |
| endPattern2                                                                                                                                                                                           | \\s\*\$\\s\*-{20}.\*                                                                                                                                                                                  |
| endPattern3                                                                                                                                                                                           | \\s\*\$\\s\*                                                                                                                                                                                          |
| endPattern4                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | basisecp.xml                                                                                                                                                                                          |

######Template attributes

**Input.**

    -------------------------
    ECP PARAMETER INFORMATION
    -------------------------

     Group 1, Type Ru ECP SD(28,MWB) (replacing 28 core electrons, lmax=4)

    Atom   0Ru   ECP group =>   1
        
        

**Output text.**

```xml
<comment class="example.output" id="basisecp">
        <module cmlx:templateRef="basisecp">
            <module cmlx:templateRef="basisgroups">
               <list cmlx:templateRef="group">
                  <list>
                     <scalar dataType="xsd:integer" dictRef="o:group">1</scalar>
                     <scalar dataType="xsd:string" dictRef="cc:elementType">Ru</scalar>
                     <scalar dataType="xsd:string" dictRef="o:ecptype">ECP SD(28,MWB)</scalar>
                  </list>
               </list>
            </module>
            <module cmlx:templateRef="atombasis">
               <list cmlx:templateRef="missingID">
                  <list>
                     <scalar dataType="xsd:integer" dictRef="cc:serial">0</scalar>
                     <scalar dataType="xsd:string" dictRef="cc:elementType">Ru</scalar>
                     <scalar dataType="xsd:integer" dictRef="o:group">1</scalar>
                  </list>
               </list>
            </module>
         </module>
    </comment>
```
