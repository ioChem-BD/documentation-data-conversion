# wave.specs {#wave.specs-d3e28870}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | MOLCAS log                                                                                                                                                                                            |
| id                                                                                                                                                                                                    | wave.specs                                                                                                                                                                                            |
| name                                                                                                                                                                                                  | Wave function specifications                                                                                                                                                                          |
| pattern                                                                                                                                                                                               | .\*Wave\\sfunction\\sspecifications:.\*                                                                                                                                                               |
| endPattern                                                                                                                                                                                            | \\s\*\\-\\-\\s\*                                                                                                                                                                                      |
| endPattern2                                                                                                                                                                                           | \\s\*\$((?!Number).)\*                                                                                                                                                                                |
| endPattern3                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | modules/wave.specs.xml                                                                                                                                                                                |

######Template attributes

**Input.**

       
    ++       Wave function specifications:
          Wave function specifications:
          -----------------------------

          Number of closed shell electrons          14
          Number of electrons in active shells       4
          Max number of holes in RAS1 space          0
          Max nr of electrons in RAS3 space          0
          Number of inactive orbitals                7
          Number of active orbitals                  4
          Number of secondary orbitals             105
          Spin quantum number                      0.0
          State symmetry                             1

    --
        

**Output text.**

```xml
<comment class="example.output" id="wave.specs">
         <module cmlx:templateRef="wave.specs">
            <scalar dataType="xsd:integer" dictRef="m:closedelec">14</scalar>
            <scalar dataType="xsd:integer" dictRef="m:activeelec">4</scalar>
            <scalar dataType="xsd:integer" dictRef="m:ras1holes">0</scalar>
            <scalar dataType="xsd:integer" dictRef="m:ras3holes">0</scalar>
            <scalar dataType="xsd:integer" dictRef="m:inactiveorbitals">7</scalar>
            <scalar dataType="xsd:integer" dictRef="m:activeorbitals">4</scalar>
            <scalar dataType="xsd:integer" dictRef="m:secondaryorbitals">105</scalar>
            <scalar dataType="xsd:double" dictRef="m:spinquantumnum">0.0</scalar>
            <scalar dataType="xsd:integer" dictRef="m:statesymm">1</scalar>
         </module>    
    </comment>
```
