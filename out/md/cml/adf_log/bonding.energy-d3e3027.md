# bonding.energy {#bonding.energy-d3e3027}

ADF log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | bonding.energy                                                                                                                                      |
| name                                                                                                                                                | Bonding energy section                                                                                                                              |
| pattern                                                                                                                                             | \\s\*B\\sO\\sN\\sD\\sI\\sN\\sG\\s+E\\sN\\sE\\sR\\sG\\sY.\*                                                                                          |
| endPattern                                                                                                                                          | \\s\*\$\\s\*\$\\s\*\\={5,}+.\*                                                                                                                      |
| offset                                                                                                                                              | -1                                                                                                                                                  |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | bonding.energy.xml                                                                                                                                  |

######Template attributes

**Input.**

     ===========================
     B O N D I N G   E N E R G Y  ***  (decomposition)  ***
     ===========================

    *** WARNING ***

    The bond energy is computed as an energy difference between molecule and
    fragments. In particular when the fragments are single atoms, they are usually
    computed as SPHERICALLY SYMMETRIC and SPIN-RESTRICTED. Obviously, this usually
    does NOT represent the true atomic groundstate.
    ...

    Summary of Bonding Energy (energy terms are taken from the energy decomposition above)
    ======================================================================================

      Electrostatic Energy:            -33.475567726025723       -910.9165        -21006.24        -87890.09
      Kinetic Energy:                   24.937087958477719        678.5727         15648.26         65472.32
      Coulomb (Steric+OrbInt) Energy:    8.680505521299182        236.2086          5447.10         22790.66
      XC Energy:                       -27.291167088981922       -742.6304        -17125.47        -71652.95
      Solvation:                        -0.008061655700173         -0.2194            -5.06           -21.17
      Dispersion Energy:                -0.128691164634089         -3.5019           -80.75          -337.88
      Spin-Orbit:                       -0.149130118381270         -4.0580           -93.58          -391.54
                                      --------------------     -----------       ----------      -----------
      Total Bonding Energy:            -27.149141335230745       -738.7657        -17036.35        -71280.06

     ...

        

**Output text.**

```xml
<comment class="example.output" id="bonding.energy">
     <module cmlx:lineCount="13" cmlx:templateRef="summary">
      <scalar dataType="xsd:double" dictRef="cc:eener" units="nonsi:electronvolt">-910.9165</scalar>
      <scalar dataType="xsd:double" dictRef="cc:kinener" units="nonsi:electronvolt">678.5727</scalar>
      <scalar dataType="xsd:double" dictRef="cc:coulombener" units="nonsi:electronvolt">236.2086</scalar>
      <scalar dataType="xsd:double" dictRef="cc:xcener" units="nonsi:electronvolt">-742.6304</scalar>
      <scalar dataType="xsd:double" dictRef="cc:solvener" units="nonsi:electronvolt">-0.2194</scalar>
      <scalar dataType="xsd:double" dictRef="cc:dispener" units="nonsi:electronvolt">-3.5019</scalar>
      <scalar dataType="xsd:double" dictRef="cc:spinener" units="nonsi:electronvolt">-4.058</scalar>
      <scalar dataType="xsd:double" dictRef="cc:total" units="nonsi:electronvolt">-738.7657</scalar>
     </module>
    </comment>
```
