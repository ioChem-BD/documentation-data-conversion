# orbitals {#orbitals-d3e24347}

Turbomole log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole log                                                                                                                                       |
| id                                                                                                                                                  | orbitals                                                                                                                                            |
| name                                                                                                                                                | Molecular orbitals                                                                                                                                  |
| pattern                                                                                                                                             | \\s\*mo\\soccupation.\*                                                                                                                             |
| endPattern                                                                                                                                          | \\s\*number\\sof\\soccupied\\sorbitals.\*                                                                                                           |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | orbitals.xml                                                                                                                                        |

######Template attributes

**Input.**

        mo occupation :
       irrep   mo's   occupied
        a      576      135
     
     number of basis functions   :          576
     number of occupied orbitals :          135
        

**Input.**

        mo occupation :
       irrep   mo's   occupied
        a      394       79
        b      389       76
     
     number of basis functions   :          783
     number of occupied orbitals :          155
        

**Output text.**

```xml
<comment class="example.output" id="orbitals">
       <module cmlx:lineCount="6" cmlx:templateRef="orbitals">
        <list cmlx:lineCount="1" cmlx:templateRef="mooccupation">
         <array dataType="xsd:string" dictRef="t:irrep" size="1">a</array>
         <array dataType="xsd:integer" dictRef="t:numberofmos" size="1">576</array>
         <array dataType="xsd:integer" dictRef="t:occupiedmos" size="1">135</array>
        </list>
        <scalar dataType="xsd:integer" dictRef="t:basisnumber">576</scalar>
        <scalar dataType="xsd:integer" dictRef="t:occupied">135</scalar>
       </module>     
    </comment>
```

**Output text.**

```xml
<comment class="example.output2" id="orbitals">
       <module cmlx:lineCount="7" cmlx:templateRef="orbitals">
        <list cmlx:lineCount="2" cmlx:templateRef="mooccupation">
         <array dataType="xsd:string" dictRef="t:irrep" size="2">a b</array>
         <array dataType="xsd:integer" dictRef="t:numberofmos" size="2">394 389</array>
         <array dataType="xsd:integer" dictRef="t:occupiedmos" size="2">79 76</array>
        </list>
        <scalar dataType="xsd:integer" dictRef="t:basisnumber">783</scalar>
        <scalar dataType="xsd:integer" dictRef="t:occupied">155</scalar>
     </module> 
    </comment>
```
