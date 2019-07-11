# kirkwood {#kirkwood-d3e29027}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | kirkwood                                                                                                                                            |
| name                                                                                                                                                | Kirkwood model                                                                                                                                      |
| pattern                                                                                                                                             | \\s\*Reaction\\sField\\scalculation:\\sthe\\sKirkwood\\smodel.\*                                                                                    |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| xml:base                                                                                                                                            | modules/kirkwood.xml                                                                                                                                |

######Template attributes

**Input.**

         Reaction Field calculation: the Kirkwood model
          Dielectric Constant : 0.800E+02
          Eps_opt             : 0.100E+01
          Radius of Cavity(au): 0.475E+01
          l_Max               : 4
          Calculation type    : equilibrium 
     
        

**Output text.**

```xml
<comment class="example.output" id="kirkwood">
        <module cmlx:templateRef="kirkwood">
            <scalar dataType="xsd:double" dictRef="m:dielectricvalue">0.800E+02</scalar>
            <scalar dataType="xsd:double" dictRef="m:epsopt">0.100E+01</scalar>
            <scalar dataType="xsd:double" dictRef="m:cavityradius" units="nonsi:angstrom">0.475E+01</scalar>
            <scalar dataType="xsd:double" dictRef="m:lmax">4</scalar>
            <scalar dataType="xsd:string" dictRef="m:calctype">equilibrium</scalar>
        </module> 
    </comment>
```
