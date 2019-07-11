# adf.runtype {#adf.runtype-d3e1531}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | adf.runtype                                                                                                                                         |
| pattern                                                                                                                                             | \\s+\\\*\\s+R\\sU\\sN\\s+T\\sY\\sP\\sE\\s\\:.\*                                                                                                     |
| endPattern                                                                                                                                          | \\s\*\\\*{80,}.\*                                                                                                                                   |
| offset                                                                                                                                              | -1                                                                                                                                                  |
| endOffset                                                                                                                                           | 2                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | runtype/runtype.xml                                                                                                                                 |

######Template attributes

**Input.**

                           ************************************
                           *  R U N   T Y P E : SINGLE POINT  *
                           ************************************

     ===============
     G E O M E T R Y  ***  Planar Molecule  ***
     ===============
      

     ATOMS
     =====                            X Y Z                    CHARGE
                                    (Angstrom)             Nucl     +Core       At.Mass
                           --------------------------    ----------------       -------
        1  O               0.0000    0.0000    0.0000      8.00      6.00       15.9949
        2  H               0.0000   -0.6894   -0.5785      1.00      1.00        1.0078
        3  H               0.0000    0.6894   -0.5785      1.00      1.00        1.0078
    ...

    =====================================
     S Y M M E T R Y ,   E L E C T R O N S
     =====================================
     ...


     ***************************************************************************************************    
        
        

**Output text.**

```xml
<comment class="example.output" id="adf.runType">
      <module cmlx:lineCount="241" cmlx:templateRef="adf.runtype">       
       <scalar dataType="xsd:string" dictRef="cc:runtype">SINGLE POINT</scalar>
         <module cmlx:lineCount="12" cmlx:templateRef="geometry">
          <molecule id="a25">
            <atomArray>
              <atom id="a1" elementType="O" x3="0.0" y3="0.0" z3="0.0">
                <scalar dataType="xsd:integer" dictRef="cc:serial">1</scalar>
                <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">8</scalar>
              </atom>
              <atom id="a2" elementType="H" x3="0.0" y3="-0.6894" z3="-0.5785">
                <scalar dataType="xsd:integer" dictRef="cc:serial">2</scalar>
                <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
              </atom>
              <atom id="a3" elementType="H" x3="0.0" y3="0.6894" z3="-0.5785">
                <scalar dataType="xsd:integer" dictRef="cc:serial">3</scalar>
                <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
              </atom>
            </atomArray>
            <formula formalCharge="0" concise="H 2 O 1">
              <atomArray elementType="H O" count="2.0 1.0" />
            </formula>
            <bondArray>
              <bond atomRefs2="a1 a2" id="a1_a2" order="S" />
              <bond atomRefs2="a1 a3" id="a1_a3" order="S" />
            </bondArray>
            <property dictRef="cml:molmass">
              <scalar dataType="xsd:double" units="unit:dalton">18.01528</scalar>
            </property>
          </molecule>
        </module>
      </module>
    </comment>
```

-   [geometry](/out/md/cml/adf_log/geometry-d3e1546.md)

<!-- -->

-   [symmetry](/out/md/cml/adf_log/symmetry-d3e1880.md)
