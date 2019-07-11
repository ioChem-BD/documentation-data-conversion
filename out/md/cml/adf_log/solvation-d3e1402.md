# solvation {#solvation-d3e1402}

ADF log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | solvation                                                                                                                                           |
| name                                                                                                                                                | ADF Init solvation parameters                                                                                                                       |
| pattern                                                                                                                                             | \\s\*SOLVATION.\*\$\\-\\-\\-.\*                                                                                                                     |
| endPattern                                                                                                                                          | \\s\*\$\\-\\-\\-.\*                                                                                                                                 |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | solvation.xml                                                                                                                                       |

######Template attributes

**Input.**

     SOLVATION
    -------------------------------------------

      The Solvent-Excluding surface is calculated

           Division Level for Surface Triangles (NDIV)                  5
           Final Division Level for Triangles (NFDIV)                   1
           Radius of the Solvent (RSOL)                           1.40000 angstr
           Minimum Radius for new sphere (RMINSOLV)               0.50000 angstr
           Overlapping Factor (OFAC)                              0.80000
           New spheres will be assigned to the initials using ASSG1

      Dielectric Constant (EPSL)                                 78.40000

           COSMO equation is solved iteratively-               conjugate-gradient

           Maximun of Iterations for Charges (NCIX)                  1000
           Criterion for Charge convergence (CCNV)                1.0E-10

      Geometry-dependent empirical factor                         0.00000

      COSMO charges included variationally in SCF

           COSMO started at end of SCF

      C-Matrix calculated in cspmtx

      In cspmtx, C-Matrix calculated using fitted potential

    -------------------------------------------
        

**Output text.**

```xml
<comment class="example.output" id="solvation">
        <module cmlx:lineCount="30" cmlx:templateRef="solvation">
          <list id="cosmo">
                <scalar dataType="xsd:integer" dictRef="a:ndiv">5</scalar>
                <scalar dataType="xsd:integer" dictRef="a:nfdiv">1</scalar>
                <scalar dataType="xsd:double" dictRef="a:rsol" units="nonsi:angstrom">1.4</scalar>
                <scalar dataType="xsd:double" dictRef="a:rminsolv" units="nonsi:angstrom">0.5</scalar>
                <scalar dataType="xsd:double" dictRef="a:ofac">0.8</scalar>
                <scalar dataType="xsd:double" dictRef="a:epsl">78.4</scalar>
                <scalar dataType="xsd:string" dictRef="a:cosmomethod">conjugate-gradient</scalar>
                <scalar dataType="xsd:double" dictRef="a:ncix">1000.0</scalar>
                <scalar dataType="xsd:double" dictRef="a:ccnv">1.0E-10</scalar>
                <scalar dataType="xsd:double" dictRef="a:gdsf">0.0</scalar>
            </list>
        </module>     
    </comment>
```
