# Page components detail

# General Info

| Field                                                                                   | Source                                                                                 | Sample value                                                                                                          |
|----|----|----|
| Title                                                                                   | *Set on Browse calculation publication*                                                | supercell2x2x2                                                                                                        |
| Browse Item                                                                             | *URL pointing Browse published item*                                                   | https://www.iochem-bd.org/handle/10/123456                                                                            |
| Program                                                                                 | [header template](/out/md/cml/quantumespresso_log/header-d3e33197.md)                                                    | QuantumEspresso 6.1                                                                                                   |
| Author                                                                                  | *Username fullname*                                                                    | Alvarez Moreno, Moises                                                                                                |
| Formula                                                                                 | *Atom count from final geometry*                                                       | Bi 32 O 128 V 32                                                                                                      |
| Calculation type                                                                        | Custom logic                                                                           | Geometry optimization                                                                                                 |
| Method                                                                                  | Method used (fixed)                                                                    | DFT                                                                                                                   |
| Functional                                                                              | Custom logic                                                                           | Extracted from the initial section in [parameters template](/out/md/cml/quantumespresso_log/parameters-d3e33261.md)                                     |

######QuantumEspresso - General Info - Main fields

| Field                                                                                             | Source                                                                                            | Sample value                                                                                      |
|----|----|----|
| Temperature                                                                                       | [\<scalar dictRef=\"cc:parameter\"\>static permittivity\</scalar\>](/out/md/cml/quantumespresso_log/environ-d3e34039.md)            | 298.87222246132 K                                                                                 |
| Pressure                                                                                          | [\<scalar dictRef=\"cc:parameter\"\>external pressure in input\</scalar\>](/out/md/cml/quantumespresso_log/environ-d3e34039.md)     | -3454.231433506 atm                                                                               |

######QuantumEspresso- General Info - Additional fields (if they appear in [environ](/out/md/cml/quantumespresso_log/environ-d3e34039.md) module)

![](/imgs/QUANTUMESPRESSO_header.png)

[^1]

[^2]

# Settings

Most relevant calculation input parameters. All information fields come from [\<module cmlx:templateRef=\"parameters\"\>](/out/md/cml/quantumespresso_log/parameters-d3e33261.md)

-   bravais-lattice index

-   lattice parameter (alat)

-   unit-cell volume

-   number of atoms/cell

-   number of atomic types

-   number of electrons

-   number of Kohn-Sham states

-   kinetic-energy cutoff

-   charge density cutoff

-   convergence threshold

-   mixing beta

-   number of iterations used

-   Exchange-correlation

-   \...

![](/imgs/QUANTUMESPRESSO_settings.png)

# Atoms and Basis Sets

After settings section, our HTML resume will output cell coordinates, lattice vectors and a coordinates table with molecule atoms.

Geometry is readed from input file using :[\<list cmlx:templateRef=\"atoms\"\>](/out/md/cml/quantumespresso_log/qespresso.input-d3e40265.md), [\<list cmlx:templateRef=\"species\"\>](/out/md/cml/quantumespresso_log/qespresso.input-d3e40265.md), [\<module cmlx:templateRef=\"lattice\"\>](#lattice-d3e33441) and [\<module cmlx:templateRef=\"axes\"\>](/out/md/cml/quantumespresso_log/axes-d3e33547.md) for
geometry optimizations.

For every atom, we will output it\'s serial number, atom type, cartesian and fractional coordinates (in angstroms) , and [\<list cmlx:templateRef=\"species\"\>](/out/md/cml/quantumespresso_log/qespresso.input-d3e40265.md).

![](/imgs/QUANTUMESPRESSO_geometry.png)

# Molecular Info

This section captures molecule additional information not captured on previous section.

## LDA+U calculation

Data source: [\<module cmlx:templateRef=\'ldau\'\>](/out/md/cml/quantumespresso_log/ldau-d3e34327.md)

![](/imgs/QUANTUMESPRESSO_info_ldau.png)

## Kpoint list

Data source: [\<module cmlx:templateRef=\'kpoints\'\>](/out/md/cml/quantumespresso_log/kpoints-d3e34371.md)

![](/imgs/QUANTUMESPRESSO_kpoints.png)

## Point group

Data source: [\<module cmlx:templateRef=\'point.group\'\>](/out/md/cml/quantumespresso_log/point.group-d3e34017.md)

![](/imgs/QUANTUMESPRESSO_point_group.png)

# Modules

## Forces

Data source: [\<module cmlx:templateRef=\'forces\'\>](/out/md/cml/quantumespresso_log/forces-d3e34423.md)

![](/imgs/QUANTUMESPRESSO_module_forces.png)

## Energies

Data source: [\<module cmlx:templateRef=\'energies\'\>](/out/md/cml/quantumespresso_log/energies-d3e34218.md)

![](/imgs/QUANTUMESPRESSO_module_energies.png)

## Magnetic moment per site

Data source: [\<module cmlx:templateRef=\'magnetic\'\>](/out/md/cml/quantumespresso_log/magnetic-d3e34480.md)

![](/imgs/QUANTUMESPRESSO_module_magnetic.png)

## Eigenvalues

Data source [\<module cmlx:templateRef=\'eigenvalues\'\>](/out/md/cml/quantumespresso_log/eigenvalues-d3e34514.md)

![](/imgs/QUANTUMESPRESSO_module_eigen.png)

## Projects wavefunctions onto orthogonalized atomic wavefunctions

Data source: [\<module cmlx:templateRef=\'projwfc\'\>](/out/md/cml/quantumespresso_log/projwfc.md)

![](/imgs/QUANTUMESPRESSO_module_projwfc.png)

## Frequencies

Data source: [\<module cmlx:templateRef=\'frequencies\'\>](/out/md/cml/quantumespresso_log/frequencies.md)

![](/imgs/QUANTUMESPRESSO_module_frequencies.png)

[^1]: string `qex:getCalcType` string `modName` string `calculation`

    ```xml
                                
        $modName  Name of the module <module cmlx:templateRef="header" >
        $calculation   Calculation type defined on <module cmlx:templateRef="qespresso.input" > , CONTROL section. 
                       
       <!-- Calculation type related constants -->
       <xsl:param name="moduleName"/>
       <xsl:param name="calculation"/>
            
            <xsl:variable name="nCalculation" select="replace(helper:trim(upper-case($calculation)),'[^A-Z-]','')"/>          
            
            <xsl:choose>
                <xsl:when test="helper:trim(upper-case($moduleName)) = 'PWSCF'">
                    <xsl:choose>
                        <xsl:when test="$nCalculation = 'VC-RELAX'">
                            <xsl:value-of select="$qex:GeometryOptimization"/>
                        </xsl:when>
                        <xsl:when test="$nCalculation = 'RELAX'">
                            <xsl:value-of select="$qex:GeometryOptimization"/>
                        </xsl:when>
                        <xsl:when test="$nCalculation = 'SCF'">
                            <xsl:value-of select="$qex:SinglePoint"/>
                        </xsl:when>
                        <xsl:when test="$nCalculation = 'BANDS'">
                            <xsl:value-of select="$qex:Bands"/>
                        </xsl:when>
                        <xsl:when test="$nCalculation = 'NSCF'">
                            <xsl:value-of select="$qex:NonSCF"/>
                        </xsl:when>
                        <xsl:when test="$nCalculation = 'MD'">
                            <xsl:value-of select="$qex:MolecularDynamics"/>
                        </xsl:when>
                        <xsl:when test="$nCalculation = 'CP'">
                            <xsl:value-of select="$qex:CarParrinello"/>
                        </xsl:when>
                        <xsl:when test="$nCalculation = 'CP-WF'">
                            <xsl:value-of select="$qex:CarParrinelloWF"/>
                        </xsl:when>            
                        <xsl:otherwise>
                            <xsl:value-of select="$qex:SinglePoint"/>
                        </xsl:otherwise>
                    </xsl:choose>                        
                </xsl:when>
                <xsl:when test="helper:trim(upper-case($moduleName)) = 'PWNEB'">
                    <xsl:value-of select="$qex:NudgedElasticBand"/>
                </xsl:when>
                <xsl:otherwise>
                    <xsl:value-of select="$qex:SinglePoint"/>
                </xsl:otherwise>            
            </xsl:choose>
                            
                            
    ```

[^2]: ```xml
                                
        $functionals  <module cmlx:templateRef="header" >
        $calculation   Calculation type defined on <module cmlx:templateRef="qespresso.input" > , CONTROL section. 
                       

                            
                            
    ```
