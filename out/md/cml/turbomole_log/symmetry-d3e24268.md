# symmetry {#symmetry-d3e24268}

Turbomole log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole log                                                                                                                                       |
| id                                                                                                                                                  | symmetry                                                                                                                                            |
| name                                                                                                                                                | Symmetry information                                                                                                                                |
| pattern                                                                                                                                             | \\s\*symmetry\\sgroup\\sof\\sthe\\smolecule.\*                                                                                                      |
| endPattern                                                                                                                                          | \\s\*maximum\\snumber\\sof\\sshells\\swhich\\sare\\srelated\\sby\\ssymmetry.\*                                                                      |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | symmetry.xml                                                                                                                                        |

######Template attributes

**Input.**

         symmetry group of the molecule :   d5h
        
         the group has the following generators :
           c5(z)
           c2(x)
           mirror plane sigma(xy)
        
           20 symmetry operations found
        
         there are 8 real representations :   a1'  a2'  e1'  e2'  a1"  a2"  e1"  e2" 
        
         maximum number of shells which are related by symmetry : 10
        

**Output text.**

```xml
<comment class="example.output" id="symmetry">    
        <module cmlx:lineCount="8" cmlx:templateRef="symmetry">
          <scalar dataType="xsd:string" dictRef="t:symmetryGroup">d5h</scalar>
          <list cmlx:lineCount="3" cmlx:templateRef="generators">
            <scalar dataType="xsd:string" dictRef="t:generators">c5(z)</scalar>
            <scalar dataType="xsd:string" dictRef="t:generators">c2(x)</scalar>
            <scalar dataType="xsd:string" dictRef="t:generators">mirror plane sigma(xy)</scalar>
          </list>
        </module>
    </comment>
```
