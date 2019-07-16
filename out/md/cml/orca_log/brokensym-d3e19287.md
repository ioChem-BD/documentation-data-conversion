# brokensym {#brokensym-d3e19287}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Partial.png)                                                                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Orca log                                                                                                                                                                                              |
| id                                                                                                                                                                                                    | brokensym                                                                                                                                                                                             |
| name                                                                                                                                                                                                  | Broken symmetry magnetic coupling analysis                                                                                                                                                            |
| pattern                                                                                                                                                                                               | \\s\*-+\\s\*\$\\s\*BROKEN\\sSYMMETRY\\sMAGNETIC\\sCOUPLING\\sANALYSIS.\*\$\\s\*-+\\s\*                                                                                                                |
| endPattern                                                                                                                                                                                            | \\s\*J\\(1\\):.\*                                                                                                                                                                                     |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | brokensym.xml                                                                                                                                                                                         |

######Template attributes

**Input.**

        ------------------------------------------
        BROKEN SYMMETRY MAGNETIC COUPLING ANALYSIS
        ------------------------------------------
        
        S(High-Spin)      =   1.0    
        <S**2>(High-Spin) =   2.0054    
        <S**2>(BrokenSym) =   0.9478    
        E(High-Spin)      = -3947.379193 Eh
        E(BrokenSym)      = -3947.384041 Eh
        E(High-Spin)-E(BrokenSym)= 0.1319 eV   1063.881 cm**-1 (ANTIFERROMAGNETIC coupling)
        
                  ---------------------------------------------------------
                  I Spin-Hamiltonian Analysis based on H(HDvV)= -2J*SA*SB I
            -------                                                       -----------
            I J(1) =   -1063.88 cm**-1    (from -(E[HS]-E[BS])/Smax**2)             I
            I J(2) =    -531.94 cm**-1    (from -(E[HS]-E[BS])/(Smax*(Smax+1))      I
            I J(3) =   -1005.96 cm**-1    (from -(E[HS]-E[BS])/(<S**2>HS-<S**2>BS)) I
            -------------------------------------------------------------------------
        
          J(1): (a) A.P. Ginsberg J. Am. Chem. Soc. 102 (1980), 111
                (b) L. Noodleman J. Chem. Phys. 74 (1981), 5737
                (c) L. Noodleman E.R. Davidson Chem. Phys. 109 (1985), 131
          J(2)  (d) A. Bencini D. Gatteschi J. Am. Chem. Soc. 108 (1980), 5763
          J(3)  (e) K. Yamaguchi Y. Takahara T. Fueno in: V.H. Smith (Ed.)
                    Applied Quantum Chemistry. Reidel, Dordrecht (1986), pp 155
                (f) T.Soda et al. Chem. Phys. Lett., 319, (2000), 223
        

**Output text.**

```xml
<comment class="example.output" id="brokensym">
      <module cmlx:templateRef="brokensym">
         <list cmlx:templateRef="spinHamiltonianAnalyis">
            <array dataType="xsd:integer" dictRef="o:jindex" size="3">1 2 3</array>
            <array dataType="xsd:double" dictRef="cc:value" size="3" units="nonsi:cm-1">-1063.88 -531.94 -1005.96</array>
         </list>
         <scalar dataType="xsd:double" dictRef="o:sHighSpin">1.0</scalar>
         <scalar dataType="xsd:double" dictRef="o:s2HighSpin">2.0054</scalar>
         <scalar dataType="xsd:double" dictRef="o:s2BrokenSym">0.9478</scalar>
         <scalar dataType="xsd:double" dictRef="o:eHighSpin" units="nonsi:hartree">-3947.379193</scalar>
         <scalar dataType="xsd:double" dictRef="o:eBrokenSym" units="nonsi:hartree">-3947.384041</scalar>
         <scalar dataType="xsd:double" dictRef="o:ediff" units="nonsi:cm-1">1063.881</scalar>
      </module>
    </comment>
```
