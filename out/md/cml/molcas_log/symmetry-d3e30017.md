# symmetry {#symmetry-d3e30017}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | symmetry                                                                                                                                            |
| name                                                                                                                                                | Symmetry information                                                                                                                                |
| pattern                                                                                                                                             | \\s\*\\+\\+\\s\*Symmetry\\sinformation.\*                                                                                                           |
| pattern2                                                                                                                                            | \\s\*\\-\\-\\-\\s\*Group\\sGenerators\\s\*\\-\\-\\-\\s\*                                                                                            |
| endPattern                                                                                                                                          | \\s\*\\-\\-\\s\*                                                                                                                                    |
| endPattern2                                                                                                                                         | \\s{10,}\\S+.\*\$\\s{0,5}\\S+.\*                                                                                                                    |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/symmetry.xml                                                                                                                                |

######Template attributes

**Input.**

    ++    Symmetry information:
    ---------------------

                  --- Group Generators ---
                  Reflection in the yz-plane  
                  Reflection in the xz-plane  
                  Reflection in the xy-plane  

                  Character Table for D2h

                           E   s(yz) s(xz) C2(z) s(xy) C2(y) C2(x)   i  
                  ag       1     1     1     1     1     1     1     1  
                  b3u      1    -1     1    -1     1    -1     1    -1  x
                  b2u      1     1    -1    -1     1     1    -1    -1  y
                  b1g      1    -1    -1     1     1    -1    -1     1  xy, Rz
                  b1u      1     1     1     1    -1    -1    -1    -1  z
                  b2g      1    -1     1    -1    -1     1    -1     1  xz, Ry
                  b3g      1     1    -1    -1    -1    -1     1     1  yz, Rx
                  au       1    -1    -1     1    -1     1     1    -1  I
    --
        

**Output text.**

```xml
<comment class="example.output" id="symmetry">
         <module cmlx:templateRef="symmetry">
            <scalar dataType="xsd:string" dictRef="m:symmdesc">Reflection in the yz-plane</scalar>
            <scalar dataType="xsd:string" dictRef="m:symmdesc">Reflection in the xz-plane</scalar>
            <scalar dataType="xsd:string" dictRef="m:symmdesc">Reflection in the xy-plane</scalar>
            <module cmlx:templateRef="charactertable">            
               <list dictRef="m:symelemexample">
                  <scalar dataType="xsd:string" dictRef="m:symelemexample" />
                  <scalar dataType="xsd:string" dictRef="m:symelemexample">x</scalar>
                  <scalar dataType="xsd:string" dictRef="m:symelemexample">y</scalar>
                  <scalar dataType="xsd:string" dictRef="m:symelemexample">xy, Rz</scalar>
                  <scalar dataType="xsd:string" dictRef="m:symelemexample">z</scalar>
                  <scalar dataType="xsd:string" dictRef="m:symelemexample">xz, Ry</scalar>
                  <scalar dataType="xsd:string" dictRef="m:symelemexample">yz, Rx</scalar>
                  <scalar dataType="xsd:string" dictRef="m:symelemexample">I</scalar>
               </list>           
               <scalar dataType="xsd:string" dictRef="m:symmelemdesc">D2h</scalar>
               <array dataType="xsd:string" dictRef="m:symmelementrow" size="8">E s(yz) s(xz) C2(z) s(xy) C2(y) C2(x) i</array>
               <array dataType="xsd:string" dictRef="m:irreductiblerepcol" size="8">ag b3u b2u b1g b1u b2g b3g au</array>
               
               <matrix cols="8" dataType="xsd:integer" dictRef="m:characters" rows="8">1 1 1 1 1 1 1 1 1 -1 1 -1 1 -1 1 -1 1 1 -1 -1 1 1 -1 -1 1 -1 -1 1 1 -1 -1 1 1 1 1 1 -1 -1 -1 -1 1 -1 1 -1 -1 1 -1 1 1 1 -1 -1 -1 -1 1 1 1 -1 -1 1 -1 1 1 -1</matrix>
            </module>
         </module>
    </comment>
```
