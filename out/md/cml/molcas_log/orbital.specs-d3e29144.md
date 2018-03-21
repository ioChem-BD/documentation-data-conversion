# orbital.specs {#orbital.specs-d3e29144}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | orbital.specs                                                                                                                                       |
| name                                                                                                                                                | Orbital specifications                                                                                                                              |
| pattern                                                                                                                                             | .\*Orbital\\sspecifications\\s\*:\\s\*                                                                                                              |
| endPattern                                                                                                                                          | \\s\*\\-\\-\\s\*                                                                                                                                    |
| endPattern2                                                                                                                                         | .\*\[0-9\]+\$\\s\*                                                                                                                                  |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/orbital.specs.xml                                                                                                                           |

######Template attributes

**Input.**

    ++    Orbital specifications:
          -----------------------
     
          Symmetry species               1
                                         a
          Frozen orbitals                0
          Occupied orbitals             16
          Secondary orbitals            28
          Deleted orbitals               0
          Total number of orbitals      44
          Number of basis functions     44
    --
        
        

**Input.**

         Orbital specifications :
          Symmetry species               1   2
                                         a   b
          Frozen orbitals                0   0
          Aufbau                        52
          Start temperature = 0.500
          End temperature   = 0.010
          Temperature Factor= 0.460
          Deleted orbitals               0   0
          Total number of orbitals      72  70
          Number of basis functions     72  70
          
        

**Input.**

    ++       Orbital specifications:
          -----------------------

          Symmetry species                           1   2
                                                     a   b
          Frozen orbitals                            0   0
          Inactive orbitals                         27  24
          Active orbitals                            2   0
          RAS1 orbitals                              0   0
          RAS2 orbitals                              2   0
          RAS3 orbitals                              0   0
          Secondary orbitals                        91  92
          Deleted orbitals                           0   0
          Number of basis functions                120 116

    --
        

**Output text.**

```xml
<comment class="example.output" id="orbital.specs">
         <module cmlx:templateRef="orbital.specs">
            <array dataType="xsd:integer" dictRef="m:symserial" size="1">1</array>
            <array dataType="xsd:string" dictRef="m:symlabel" size="1">a</array>
            <array dataType="xsd:integer" dictRef="m:frozenorb" size="1">0</array>
            <array dataType="xsd:integer" dictRef="m:occuporb" size="1">16</array>
            <array dataType="xsd:integer" dictRef="m:secondaryorb" size="1">28</array>
            <array dataType="xsd:integer" dictRef="m:deletedorb" size="1">0</array>
            <array dataType="xsd:integer" dictRef="m:orbno" size="1">44</array>
            <array dataType="xsd:integer" dictRef="m:basisno" size="1">44</array>
         </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="orbital.specs2">
        <module cmlx:templateRef="orbital.specs">
            <array dataType="xsd:integer" dictRef="m:symserial" size="2">1 2</array>
            <array dataType="xsd:string" dictRef="m:symlabel" size="2">a b</array>
            <array dataType="xsd:integer" dictRef="m:frozenorb" size="2">0 0</array>
            <module cmlx:templateRef="aufbau">
               <scalar dataType="xsd:double" dictRef="m:tempstart">0.500</scalar>
               <scalar dataType="xsd:double" dictRef="m:tempend">0.010</scalar>
               <scalar dataType="xsd:double" dictRef="m:tempfactor">0.460</scalar>
            </module>
            <array dataType="xsd:integer" dictRef="m:deletedorb" size="2">0 0</array>
            <array dataType="xsd:integer" dictRef="m:orbno" size="2">120 116</array>
            <array dataType="xsd:integer" dictRef="m:basisno" size="2">120 116</array>
         </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="orbital.specs3">
         <module cmlx:templateRef="orbital.specs">
            <array dataType="xsd:integer" dictRef="m:symserial" size="2">1 2</array>
            <array dataType="xsd:string" dictRef="m:symlabel" size="2">a b</array>
            <array dataType="xsd:integer" dictRef="m:frozenorb" size="2">0 0</array>
            <array dataType="xsd:integer" dictRef="m:inactiveorb" size="2">27 24</array>
            <array dataType="xsd:integer" dictRef="m:activeorb" size="2">2 0</array>
            <array dataType="xsd:integer" dictRef="m:ras1orb" size="2">0 0</array>
            <array dataType="xsd:integer" dictRef="m:ras2orb" size="2">2 0</array>
            <array dataType="xsd:integer" dictRef="m:ras3orv" size="2">0 0</array>
            <array dataType="xsd:integer" dictRef="m:secondaryorb" size="2">91 92</array>
            <array dataType="xsd:integer" dictRef="m:deletedorb" size="2">0 0</array>
            <array dataType="xsd:integer" dictRef="m:basisno" size="2">120 116</array>
         </module>    
    </comment>
```
