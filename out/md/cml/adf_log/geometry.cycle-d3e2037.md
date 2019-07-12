# geometry.cycle {#geometry.cycle-d3e2037}

ADF log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | geometry.cycle                                                                                                                                      |
| name                                                                                                                                                | Geometry optimization cycle                                                                                                                         |
| pattern                                                                                                                                             | \\sGeometry\\sCYCLE.\*                                                                                                                              |
| pattern2                                                                                                                                            | \\s\*G\\sE\\sO\\sM\\sE\\sT\\sR\\sY\\s\*U\\sP\\sD\\sA\\sT\\sE.\*                                                                                     |
| endPattern                                                                                                                                          | .\*\$\\s\*Number\\sof\\selements\\sof\\sthe\\sdensity\\smatrix.\*                                                                                   |
| endPattern2                                                                                                                                         | (\\s\*\\S+\\s\*){11}+\\s\*\$\\s\*\\-{20,}+\\s\*                                                                                                     |
| endOffset                                                                                                                                           | 2                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | geometry.cycle.xml                                                                                                                                  |

######Template attributes

**Input.**

     =============================
     G E O M E T R Y   U P D A T E  ***  1  ***
     =============================
     ...

    --------------------------------------
    Geometry Convergence after Step   4
    --------------------------------------
    current energy                              -27.14895237 Hartree
    abs of energy change                0.00034166     0.00100000    T
    constrained gradient max            0.00178229     0.00100000    F
    constrained gradient rms            0.00030637     0.00066667    T
    gradient max                        0.00178229
    gradient rms                        0.00030637
    cart. step max                      0.00450423     0.01000000    T
    cart. step rms                      0.00098385     0.00666667    T  
    ...
        
     Coordinates (Cartesian)
     =======================

         Atom                    bohr                                 angstrom
                       X           Y           Z              X           Y           Z
     -------------------------------------------------------------------------------------
         1 Mo      0.000000   -4.459974    0.000318       0.000000   -2.360117    0.000169
         2 Mo      4.459974    0.000000    0.000318       2.360117    0.000000    0.000169
         3 Mo     -4.459974    0.000000    0.000318      -2.360117    0.000000    0.000169
         4 Mo      0.000000    4.459974    0.000318       0.000000    2.360117    0.000169
         5 Mo      0.000000    0.000000   -4.460768       0.000000    0.000000   -2.360537
         6 W       0.000000    0.000000    4.459603       0.000000    0.000000    2.359920
         7 O       0.000000    0.000000    0.001640       0.000000    0.000000    0.000868
     -------------------------------------------------------------------------------------


     Coordinates (Cartesian, in Input Orientation)
     =======================

         Atom                    bohr                                 angstrom                 Geometric Variables
                       X           Y           Z              X           Y           Z       (0:frozen, *:LT par.)
     --------------------------------------------------------------------------------------------------------------
         1 Mo     -0.000318   -4.459974    0.000000      -0.000169   -2.360117    0.000000      1       2       3
         2 Mo     -0.000318    0.000000    4.459974      -0.000169    0.000000    2.360117      4       5       6
         3 Mo     -0.000318    0.000000   -4.459974      -0.000169    0.000000   -2.360117      7       8       9
         4 Mo     -0.000318    4.459974    0.000000      -0.000169    2.360117    0.000000     10      11      12
         5 Mo      4.460768    0.000000    0.000000       2.360537    0.000000    0.000000     13      14      15
         6 W      -4.459603    0.000000    0.000000      -2.359920    0.000000    0.000000     16      17      18
         7 O      -0.001640    0.000000    0.000000      -0.000868    0.000000    0.000000     19      20      21
     --------------------------------------------------------------------------------------------------------------
     
      Number of elements of the density matrix on this node (used, total):     25057    246753
     
     
        

**Input.**

     Geometry CYCLE 1
     ==============

     Energy gradients wrt nuclear displacements
     ==========================================
     ...

     Coordinates (Cartesian)
     =======================

         Atom                    bohr                                 angstrom                 Geometric Variables
                       X           Y           Z              X           Y           Z       (0:frozen, *:LT par.)
     --------------------------------------------------------------------------------------------------------------
         1 C      -4.748701   -1.104688   -6.013399      -2.512904   -0.584576   -3.182154      1       2       3
         2 C      -4.518962    1.637904   -6.075522      -2.391332    0.866742   -3.215028      4       5       6
         3 C      -5.816176    3.015449   -4.125306      -3.077788    1.595707   -2.183018      7       8       9
         4 C       0.196292   -0.913573    7.712840       0.103873   -0.483442    4.081459     10      11      12
         5 C      -2.773029   -2.909791   -6.786550      -1.467424   -1.539795   -3.591288     13      14      15
         6 C       1.783334   -3.265805   -6.963282       0.943700   -1.728190   -3.684810     16      17      18
         7 C      -0.495078   -2.421894   -8.180332      -0.261984   -1.281611   -4.328845     19      20      21
     --------------------------------------------------------------------------------------------------------------         
        

**Output text.**

```xml
<comment class="example.output" id="geometry.cyle">
        <module cmlx:lineCount="161" cmlx:templateRef="geometry.cycle">
            <scalar dataType="xsd:integer" dictRef="cc:cycleNumber">1</scalar>
            <module cmlx:lineCount="10" cmlx:templateRef="convergence">
               <list cmlx:templateRef="energy">
                  <scalar dataType="xsd:double" dictRef="cc:energy">-27.14895237</scalar>
               </list>
               <list cmlx:templateRef="change">
                  <scalar dataType="xsd:double" dictRef="cc:current">3.4166E-4</scalar>
                  <scalar dataType="xsd:double" dictRef="cc:threshold">0.001</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:valid">T</scalar>
               </list>
               <list cmlx:templateRef="cgradmax">
                  <scalar dataType="xsd:double" dictRef="cc:current">0.00178229</scalar>
                  <scalar dataType="xsd:double" dictRef="cc:threshold">0.001</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:valid">F</scalar>
               </list>
               <list cmlx:templateRef="cgradrms">
                  <scalar dataType="xsd:double" dictRef="cc:current">3.0637E-4</scalar>
                  <scalar dataType="xsd:double" dictRef="cc:threshold">6.6667E-4</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:valid">T</scalar>
               </list>
               <list cmlx:templateRef="gradmax">
                  <scalar dataType="xsd:double" dictRef="cc:current">0.00178229</scalar>
               </list>
               <list cmlx:templateRef="gradrms">
                  <scalar dataType="xsd:double" dictRef="cc:current">3.0637E-4</scalar>
               </list>
               <list cmlx:templateRef="cstepmax">
                  <scalar dataType="xsd:double" dictRef="cc:current">0.00450423</scalar>
                  <scalar dataType="xsd:double" dictRef="cc:threshold">0.01</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:valid">T</scalar>
               </list>
               <list cmlx:templateRef="csteprms">
                  <scalar dataType="xsd:double" dictRef="cc:current">9.8385E-4</scalar>
                  <scalar dataType="xsd:double" dictRef="cc:threshold">0.00666667</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:valid">T</scalar>
               </list>
            </module>             
            <module cmlx:lineCount="30" cmlx:templateRef="coordinates">
                <scalar dataType="xsd:string" dictRef="cc:label">Cartesian</scalar>
                <molecule id="a99">
                    <atomArray>
                        <atom id="a1" elementType="Mo" x3="0.0" y3="-2.360117" z3="1.69E-4">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">1</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a2" elementType="Mo" x3="2.360117" y3="0.0" z3="1.69E-4">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">2</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a3" elementType="Mo" x3="-2.360117" y3="0.0" z3="1.69E-4">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">3</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a4" elementType="Mo" x3="0.0" y3="2.360117" z3="1.69E-4">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">4</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a5" elementType="Mo" x3="0.0" y3="0.0" z3="-2.360537">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">5</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a6" elementType="W" x3="0.0" y3="0.0" z3="2.35992">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">6</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">74</scalar>
                        </atom>
                        <atom id="a7" elementType="O" x3="0.0" y3="0.0" z3="8.68E-4">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">7</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">8</scalar>
                        </atom>
                    </atomArray>
                </molecule>
            </module>
            <module cmlx:lineCount="31" cmlx:templateRef="coordinates">
                <scalar dataType="xsd:string" dictRef="cc:label">Cartesian, in Input Orientation</scalar>
                <molecule id="a24">
                    <atomArray>
                        <atom id="a1" elementType="Mo" x3="-1.69E-4" y3="-2.360117" z3="0.0">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">1</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a2" elementType="Mo" x3="-1.69E-4" y3="0.0" z3="2.360117">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">2</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a3" elementType="Mo" x3="-1.69E-4" y3="0.0" z3="-2.360117">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">3</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a4" elementType="Mo" x3="-1.69E-4" y3="2.360117" z3="0.0">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">4</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a5" elementType="Mo" x3="2.360537" y3="0.0" z3="0.0">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">5</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">42</scalar>
                        </atom>
                        <atom id="a6" elementType="W" x3="-2.35992" y3="0.0" z3="0.0">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">6</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">74</scalar>
                        </atom>
                        <atom id="a7" elementType="O" x3="-8.68E-4" y3="0.0" z3="0.0">
                            <scalar dataType="xsd:integer" dictRef="cc:serial">7</scalar>
                            <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">8</scalar>
                        </atom>                   
                    </atomArray>
                </molecule>
            </module>
        </module>
        </comment>
```

**Output text.**

```xml
<comment class="example.output" id="geometry.cycle2">
     <module cmlx:lineCount="1911" cmlx:templateRef="geometry.cycle">
        <scalar dataType="xsd:integer" dictRef="cc:cycleNumber">1</scalar>
        <module cmlx:lineCount="105" cmlx:templateRef="coordinates">
              <scalar dataType="xsd:string" dictRef="cc:label">Cartesian</scalar>
              <molecule id="geometry.cycle">
               <atomArray>
                <atom id="a1" elementType="C" x3="-2.512904" y3="-0.584576" z3="-3.182154">
                 <scalar dataType="xsd:integer" dictRef="cc:serial">1</scalar>
                 <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                </atom>
                <atom id="a2" elementType="C" x3="-2.391332" y3="0.866742" z3="-3.215028">
                 <scalar dataType="xsd:integer" dictRef="cc:serial">2</scalar>
                 <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                </atom>
                <atom id="a3" elementType="C" x3="-3.077788" y3="1.595707" z3="-2.183018">
                 <scalar dataType="xsd:integer" dictRef="cc:serial">3</scalar>
                 <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                </atom>
                <atom id="a4" elementType="C" x3="0.103873" y3="-0.483442" z3="4.081459">
                 <scalar dataType="xsd:integer" dictRef="cc:serial">4</scalar>
                 <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                </atom>
                <atom id="a5" elementType="C" x3="-1.467424" y3="-1.539795" z3="-3.591288">
                 <scalar dataType="xsd:integer" dictRef="cc:serial">5</scalar>
                 <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                </atom>
                <atom id="a6" elementType="C" x3="0.9437" y3="-1.72819" z3="-3.68481">
                 <scalar dataType="xsd:integer" dictRef="cc:serial">6</scalar>
                 <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                </atom>
                <atom id="a7" elementType="C" x3="-0.261984" y3="-1.281611" z3="-4.328845">
                 <scalar dataType="xsd:integer" dictRef="cc:serial">7</scalar>
                 <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                </atom>
                </atomArray>
            </molecule>
            </module>
        </module>
    </comment>
```
