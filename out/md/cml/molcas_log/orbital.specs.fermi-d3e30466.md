# orbital.specs.fermi {#orbital.specs.fermi-d3e30466}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | MOLCAS log                                                                                                                                                                                            |
| id                                                                                                                                                                                                    | orbital.specs.fermi                                                                                                                                                                                   |
| name                                                                                                                                                                                                  | Fermi aufbau orbitals                                                                                                                                                                                 |
| pattern                                                                                                                                                                                               | \\s\*Fermi\\saufbau\\sprocedure\\scompleted!.\*                                                                                                                                                       |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | modules/orbital.specs.fermi.xml                                                                                                                                                                       |

######Template attributes

**Input.**

           Fermi aufbau procedure completed!
          nOcc=   28   24   
        

**Input.**

      Fermi aufbau procedure completed!
     nOcc(alpha)=                    29                    24
     nOcc(beta) =                    27                    24   
        

**Output text.**

```xml
<comment class="example.output" id="orbital.specs.fermi">
         <module cmlx:templateRef="orbital.specs.fermi">
            <list>
                <array dataType="xsd:integer" dictRef="m:occup" size="2">28 24</array>  
            </list>           
         </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="orbital.specs.fermi2">
        <module cmlx:templateRef="orbital.specs.fermi">
            <list>
               <scalar dataType="xsd:string" dictRef="m:spintype">alpha</scalar>
               <array dataType="xsd:integer" dictRef="m:occup" size="2">29 24</array>
            </list>
            <list>
               <scalar dataType="xsd:string" dictRef="m:spintype">beta</scalar>
               <array dataType="xsd:integer" dictRef="m:occup" size="2">27 24</array>
            </list>
         </module>
    </comment>
```
