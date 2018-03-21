# Page components detail

# General Info

| Field                                                                                   | Source                                                                                 | Sample value                                                                                                          |
|----|----|----|
| Title                                                                                   | *Set on Browse calculation publication*                                                | Sample calculation                                                                                                    |
| Browse Item                                                                             | *URL pointing Browse published item*                                                   | https://argo.urv.es:8080/jspui/handle/123456789/6                                                                     |
| Program                                                                                 | [header template](/out/md/cml/orca_log/header-d3e17420)                                                    | Orca 3.0.1                                                                                                            |
| Author                                                                                  | *Username fullname*                                                                    | Alvarez Moreno, Moises                                                                                                |
| Formula                                                                                 | *Atom count from final geometry*                                                       | H 2 Fe 1 O 1                                                                                                          |
| Calculation type                                                                        | Custom logic                                                                           | Geometry optimization Minimum                                                                                         |
| Method(s)                                                                               | Custom logic                                                                           | DFT ( PBE0 )                                                                                                          |

######Orca - General Info - Main fields

![](/imgs/ORCA_header.png)

[^1]

[^2]

# Modules

## Atomic coordinates

After header section, our HTML resume will output a xyz coordinates table with current molecule atoms.

For every atom, we will output it's serial number, atom type, coordinates in angstroms, basis used and contraction.

![](/imgs/ORCA_geometry.png)

## Molecular Info

This section captures molecule additional information not captured on previous section.

### 

| Field                                                                                             | Source                                                                                            | Sample value                                                                                      |
|----|----|----|
| Multiplicity                                                                                      | Readed from Mul parameter on General settings section of [scfsettings](/out/md/cml/orca_log/scfsettings-d3e20588)     | 1                                                                                                 |
|                                                                                                   | module                                                                                            |                                                                                                   |
| Charge                                                                                            | Readed from Charge parameter on General settings section of [scfsettings](/out/md/cml/orca_log/scfsettings-d3e20588)  | 0                                                                                                 |
|                                                                                                   | module                                                                                            |                                                                                                   |

######Molecular Info - Main fields

![](/imgs/ORCA_molecularinfo.png)

### Bond distances

Data source (to read molecule and calculate bonds): [&lt;module cmlx:templateRef='input'&gt;](/out/md/cml/orca_log/input-d3e17454)

Data source (to read molecule and calculate bonds): [&lt;module cmlx:templateRef='geometry'&gt;](/out/md/cml/orca_log/geometry-d3e18989)

![](/imgs/ORCA_bonddistances.png)

### Solvation input

Data source: [&lt;module cmlx:templateRef='cosmo'&gt;](/out/md/cml/orca_log/cosmo-d3e18623)

![](/imgs/ORCA_solvationinput.png)

### Restrictions in the Geometry Optimization

Data source: [&lt;module cmlx:templateRef='optsetup'&gt;](/out/md/cml/orca_log/optsetup-d3e22377)

![](/imgs/ORCA_restrictions.png)

## Total SCF energy

Data source: [&lt;module cmlx:templateRef='totalenergy'&gt;](/out/md/cml/orca_log/totalenergy-d3e20439)

Data source: [&lt;module cmlx:templateRef='mp2'&gt;](/out/md/cml/orca_log/mp2-d3e21233)

Data source: [&lt;module cmlx:templateRef='ci'&gt;](/out/md/cml/orca_log/ci-d3e21351)

Data source: [&lt;module cmlx:templateRef='d3'&gt;](/out/md/cml/orca_log/d3)

![](/imgs/ORCA_module_scfenergy.png)

## IR spectrum / Vibrational frequencies

This module will display JSpecView + JSmol plugins (using javascript libraries) working together to represent molecule IR spectrum.

Data source: [&lt;module cmlx:templateRef='vibrations'&gt;](/out/md/cml/orca_log/vibrations-d3e19272)

Data source: [&lt;module cmlx:templateRef='irspectrum'&gt;](/out/md/cml/orca_log/irspectrum-d3e19573)

![](/imgs/ORCA_module_irspectrum.png)

![](/imgs/ORCA_module_frequencies.png)

## Population analysis

Data source [&lt;module cmlx:templateRef='loewdin'&gt;](/out/md/cml/orca_log/loewdin-d3e19850)

Data source [&lt;module cmlx:templateRef='mullikenpopulation'&gt;](/out/md/cml/orca_log/mullikenpopulation-d3e19753)

![](/imgs/ORCA_module_popanal1.png)

![](/imgs/ORCA_module_popanal2.png)

## Electrostatic moments

Data source: Charge parameter on General settings section of [scfsettings](/out/md/cml/orca_log/scfsettings-d3e20588)

Data source: [&lt;module cmlx:templateRef='electricproperties'&gt;](/out/md/cml/orca_log/electricproperties-d3e20095)

![](/imgs/ORCA_module_electrostatic.png)

## Broken symmetry magnetic coupling analysis

Data source: [&lt;module cmlx:templateRef="brokensym"&gt;](/out/md/cml/orca_log/brokensym-d3e19169)

![](/imgs/ORCA_module_brokensymm.png)

## Frontier orbitals

Data source: [&lt;module cmlx:templateRef='orbitalenergies'&gt;](/out/md/cml/orca_log/orbitalenergies-d3e19659)

![](/imgs/ORCA_module_frontierorb1.png)

![](/imgs/ORCA_module_frontierorb2.png)

## Natural orbitals

Data source: [&lt;module cmlx:templateRef='natural'&gt;](/out/md/cml/orca_log/natural-d3e20223)

![](/imgs/)

## NMR Shielding tensors

Data source:

-   [&lt;module cmlx:templateRef="nmr"&gt;](/out/md/cml/orca_log/nmr-d3e21461)

![](/imgs/ORCA_module_nmr.png)

## TDHF / TDDFT

This section displays an interative chart to visualize root energies and an additional table with most relevant dominant contributions to each root

Data source: [&lt;module cmlx:templateRef='tddft'&gt;](/out/md/cml/orca_log/tddft-d3e21579)

Data source: [&lt;module cmlx:templateRef='orbitalenergies'&gt;](/out/md/cml/orca_log/orbitalenergies-d3e19659)

![](/imgs/ORCA_module_tddft1.png)

![](/imgs/ORCA_module_tddft2.png)

## g-matrix and ZFS

Data source: [&lt;module cmlx:templateRef='eprnmr'&gt;](/out/md/cml/orca_log/eprnmr-d3e21993)

![](/imgs/ORCA_module_eprnmr.png)

## Final results

Data source: [&lt;module cmlx:templateRef='totalenergy'&gt;](/out/md/cml/orca_log/totalenergy-d3e20439)

Data source: [&lt;module cmlx:templateRef='spincontamination'&gt;](/out/md/cml/orca_log/spincontamination-d3e21190)

Data source: [&lt;module cmlx:templateRef='innerenergy'&gt;](/out/md/cml/orca_log/innerenergy-d3e19426)

Data source: [&lt;module cmlx:templateRef='mp2'&gt;](/out/md/cml/orca_log/mp2-d3e21233)

Data source: [&lt;module cmlx:templateRef='ci'&gt;](/out/md/cml/orca_log/ci-d3e21351)

Data source: [&lt;module cmlx:templateRef='dftd3'&gt;](/out/md/cml/orca_log/dftd3-d3e21961)

![](/imgs/ORCA_module_finalresults1.png)

![](/imgs/ORCA_module_finalresults2.png)

![](/imgs/ORCA_module_finalresults3.png)

[^1]: string `orca:getCalcType` boolean `isOptimization` boolean `isBrokenSymm` boolean `hasVibrations` integer `negativeFrequenciesCount`

    ```xml
        $isOptimization        Refers to function orca:isOptimization($commands), which searches optimitzation keywords from <module cmlx:templateRef="input" > module  
        $isBrokenSymm          Refers to function orca:isBrokenSymm($commands)  which searches BrokenSymm keyword from <module cmlx:templateRef="input" > module
        $hasVibrations         Exists module <module cmlx:templateRef="vibrations" > ?
        $negativeFrequenciesCount   Count negative frequencies from <module cmlx:templateRef="vibrations" > ?                            
                   
        
        <!-- Calculation type related constants -->
        <xsl:variable name="orca:GeometryOptimization" select="'Geometry optimization'" />
        <xsl:variable name="orca:SinglePoint" select="'Single point'" />
        <xsl:variable name="orca:BrokenSymmetry" select="'Broken symmetry'" />    
        <xsl:variable name="orca:TransitionState" select="'TS'" />
        <xsl:variable name="orca:Minimum" select="'Minimum'"/>

        <!-- Calculation type variables -->
        <xsl:param name="isOptimization" as="xs:boolean"/>
        <xsl:param name="isBrokenSymm" as="xs:boolean"/>
        <xsl:param name="hasVibrations" as="xs:boolean"/>
        <xsl:param name="negativeFrequenciesCount" as="xs:integer"/>
        
        <xsl:variable name="type">
            <xsl:choose>
                <xsl:when test="$isOptimization">
                    <xsl:value-of select="$orca:GeometryOptimization"/>
                </xsl:when>
                <xsl:when test="$isBrokenSymm">
                    <xsl:value-of select="$orca:BrokenSymmetry"/>
                </xsl:when>
                <xsl:otherwise>
                    <xsl:value-of select="$orca:SinglePoint"/>
                </xsl:otherwise>
            </xsl:choose>     
        </xsl:variable>
        
        <xsl:variable name="type2">
            <xsl:if test="$hasVibrations">
                <xsl:choose>
                    <xsl:when test="$negativeFrequenciesCount > 0">
                        <xsl:value-of select="$orca:TransitionState"/>
                    </xsl:when>
                    <xsl:otherwise>
                        <xsl:value-of select="$orca:Minimum"/>
                    </xsl:otherwise>
                </xsl:choose>
            </xsl:if>        
        </xsl:variable>
        
        <xsl:value-of select="concat($type, ' ', $type2)"/>                              
                            
                            
    ```

[^2]: string `orca:getMehods` nodeset `section` boolean `isTddft`

    ```xml
     
            $section    Input section elements from <module cmlx:templateRef="input"> module  
            $isTddft    Refers to function orca:isTddft($commands) which searches tddft keywords from <module cmlx:templateRef="input" > module                           
                                
            <xsl:for-each select="$section/cml:array[@dictRef='cc:keywords']">
                <xsl:variable name="line" select="./text()"/>
                <xsl:for-each select="tokenize($line,'\s+')">
                    <xsl:variable name="command" select="."/>
                    <xsl:choose>
                        <xsl:when test="matches(upper-case($command), $orca:methodsRegex)">
                            <xsl:if test="$isTddft and matches(upper-case($command), '(DFT|HF)')">TD</xsl:if><xsl:value-of select="$command"/><xsl:text> </xsl:text>    
                        </xsl:when>                   
                        <xsl:when test="matches(upper-case($command),$orca:calculationLevelRegex)">
                            <xsl:if test="$isTddft">TD</xsl:if><xsl:value-of select="$orca:calculationLevels/level[@id=upper-case($command)]/@method"/><xsl:text> </xsl:text>
                        </xsl:when>
                    </xsl:choose>                             
                </xsl:for-each>
            </xsl:for-each>
            
            <xsl:variable name="blocklines" select="$section//cml:module[@cmlx:templateRef='block']/cml:scalar"/>
            <xsl:for-each select="$blocklines">
                <xsl:variable name="line" select="./text()"/>                    
                <xsl:for-each select="tokenize($line,'\s+')">
                    <xsl:variable name="command" select="."/>                
                    <xsl:choose>
                        <xsl:when test="matches(upper-case($command), $orca:methodsRegex)">
                            <xsl:if test="$isTddft and matches(upper-case($command), '(DFT|HF)')">TD</xsl:if><xsl:value-of select="$command"/><xsl:text> </xsl:text>    
                        </xsl:when>
                        <xsl:when test="matches(upper-case($command),$orca:calculationLevelRegex)">
                            <xsl:if test="$isTddft">TD</xsl:if><xsl:value-of select="$orca:calculationLevels/level[@id=upper-case($command)]/@method"/><xsl:text> </xsl:text>
                        </xsl:when>
                    </xsl:choose>             
                </xsl:for-each>                
            </xsl:for-each>
                                
                            
    ```
