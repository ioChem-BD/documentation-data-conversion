# header {#header-d3e35088}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | MOPAC log                                                                                                                                                                                             |
| id                                                                                                                                                                                                    | header                                                                                                                                                                                                |
| name                                                                                                                                                                                                  | MOPAC header                                                                                                                                                                                          |
| pattern                                                                                                                                                                                               | \\s?\\\*+\\s?\$\\s?\\\*+\\s?Site\#.\*                                                                                                                                                                 |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | header.xml                                                                                                                                                                                            |

######Template attributes

**Input.**

     *******************************************************************************
     ** Site#: 24836        For non-commercial use only     Version 16.093L 64BITS**
     *******************************************************************************
     ** Cite this program as: MOPAC2016, Version: 16.093L, James J. P. Stewart,   **
     ** Stewart Computational Chemistry, web: HTTP://OpenMOPAC.net. Days left:  87**
     *******************************************************************************
     **                                                                           **
     **                                MOPAC2016                                  **
     **                                                                           **
     *******************************************************************************

        

**Output text.**

```xml
<comment class="example.output" id="header">
        <module cmlx:templateRef="header">
          <scalar dataType="xsd:string" dictRef="cc:programSubversion">16.093L 64BITS</scalar>
          <scalar dataType="xsd:string" dictRef="cc:programVersion">2016</scalar>
       </module>     
    </comment>
```
