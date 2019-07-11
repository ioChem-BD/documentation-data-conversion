# Page components detail

# General Info

| Field                                                                                   | Source                                                                                 | Sample value                                                                                                          |
|----|----|----|
| Title                                                                                   | *Set on Browse calculation publication*                                                | Sample calculation                                                                                                    |
| Browse Item                                                                             | *URL pointing Browse published item*                                                   | https://iochem-bd.iciq.es/browse/handle/100/1722                                                                      |
| Program                                                                                 | [header template](/out/md/cml/orca_log/header-d3e17538.md)                                                    | Orca 3.0.1                                                                                                            |
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

For every atom, we will output it\'s serial number, atom type, coordinates in angstroms, basis used and contraction.

![](/imgs/ORCA_geometry.png)

## Molecular Info

This section captures molecule additional information not captured on previous section.

### 

| Field                                                                                             | Source                                                                                            | Sample value                                                                                      |
|----|----|----|
| Multiplicity                                                                                      | Readed from Mul parameter on General settings section of [scfsettings](/out/md/cml/orca_log/scfsettings-d3e21406.md)     | 1                                                                                                 |
|                                                                                                   | module                                                                                            |                                                                                                   |
| Charge                                                                                            | Readed from Charge parameter on General settings section of [scfsettings](/out/md/cml/orca_log/scfsettings-d3e21406.md)  | 0                                                                                                 |
|                                                                                                   | module                                                                                            |                                                                                                   |

######Molecular Info - Main fields

![](/imgs/ORCA_molecularinfo.png)

### Bond distances

Data source (to read molecule and calculate bonds): [\<module cmlx:templateRef=\'input\'\>](/out/md/cml/orca_log/input-d3e17572.md)

Data source (to read molecule and calculate bonds): [\<module cmlx:templateRef=\'geometry\'\>](/out/md/cml/orca_log/geometry-d3e19107.md)

![](/imgs/ORCA_bonddistances.png)

### Solvation input

Data source: [\<module cmlx:templateRef=\'cosmo\'\>](/out/md/cml/orca_log/cosmo-d3e18741.md)

![](/imgs/ORCA_solvationinput.png)

### Restrictions in the Geometry Optimization

Data source: [\<module cmlx:templateRef=\'optsetup\'\>](/out/md/cml/orca_log/optsetup-d3e23271.md)

![](/imgs/ORCA_restrictions.png)

## Total SCF energy

Data source: [\<module cmlx:templateRef=\'totalenergy\'\>](/out/md/cml/orca_log/totalenergy-d3e21257.md)

Data source: [\<module cmlx:templateRef=\'mp2\'\>](/out/md/cml/orca_log/mp2-d3e22050.md)

Data source: [\<module cmlx:templateRef=\'ci\'\>](/out/md/cml/orca_log/ci-d3e22168.md)

Data source: [\<module cmlx:templateRef=\'d3\'\>](/out/md/cml/orca_log/d3.md)

![](/imgs/ORCA_module_scfenergy.png)

## IR spectrum / Vibrational frequencies

This module will display JSpecView + JSmol plugins (using javascript libraries) working together to represent molecule IR spectrum.

Data source: [\<module cmlx:templateRef=\'vibrations\'\>](/out/md/cml/orca_log/vibrations-d3e19390.md)

Data source: [\<module cmlx:templateRef=\'irspectrum\'\>](/out/md/cml/orca_log/irspectrum-d3e19695.md)

![](/imgs/ORCA_module_irspectrum.png)

![](/imgs/ORCA_module_frequencies.png)

## Population analysis

Data source [\<module cmlx:templateRef=\'loewdin\'\>](/out/md/cml/orca_log/loewdin-d3e20667.md)

Data source [\<module cmlx:templateRef=\'mullikenpopulation\'\>](/out/md/cml/orca_log/mullikenpopulation-d3e20570.md)

![](/imgs/ORCA_module_popanal1.png)

![](/imgs/ORCA_module_popanal2.png)

## Electrostatic moments

Data source: Charge parameter on General settings section of [scfsettings](/out/md/cml/orca_log/scfsettings-d3e21406.md)

Data source: [\<module cmlx:templateRef=\'electricproperties\'\>](/out/md/cml/orca_log/electricproperties-d3e20913.md)

![](/imgs/ORCA_module_electrostatic.png)

## Broken symmetry magnetic coupling analysis

Data source: [\<module cmlx:templateRef=\"brokensym\"\>](/out/md/cml/orca_log/brokensym-d3e19287.md)

![](/imgs/ORCA_module_brokensymm.png)

## Frontier orbitals

Data source: [\<module cmlx:templateRef=\'orbitalenergies\'\>](/out/md/cml/orca_log/orbitalenergies-d3e20476.md)

![](/imgs/ORCA_module_frontierorb1.png)

![](/imgs/ORCA_module_frontierorb2.png)

## Natural orbitals

Data source: [\<module cmlx:templateRef=\'natural\'\>](/out/md/cml/orca_log/natural-d3e21040.md)

![](/imgs/)

## NMR Shielding tensors

Data source:

-   [\<module cmlx:templateRef=\"nmr\"\>](/out/md/cml/orca_log/nmr-d3e22355.md)

![](/imgs/ORCA_module_nmr.png)

## TDHF / TDDFT

This section displays an interative chart to visualize root energies and an additional table with most relevant dominant contributions to each root

Data source: [\<module cmlx:templateRef=\'tddft\'\>](/out/md/cml/orca_log/tddft-d3e22474.md)

Data source: [\<module cmlx:templateRef=\'orbitalenergies\'\>](/out/md/cml/orca_log/orbitalenergies-d3e20476.md)

![](/imgs/ORCA_module_tddft1.png)

![](/imgs/ORCA_module_tddft2.png)

## g-matrix and ZFS

Data source: [\<module cmlx:templateRef=\'eprnmr\'\>](/out/md/cml/orca_log/eprnmr-d3e22887.md)

![](/imgs/ORCA_module_eprnmr.png)

## Final results

Data source: [\<module cmlx:templateRef=\'totalenergy\'\>](/out/md/cml/orca_log/totalenergy-d3e21257.md)

Data source: [\<module cmlx:templateRef=\'spincontamination\'\>](/out/md/cml/orca_log/spincontamination-d3e22007.md)

Data source: [\<module cmlx:templateRef=\'innerenergy\'\>](/out/md/cml/orca_log/innerenergy-d3e19548.md)

Data source: [\<module cmlx:templateRef=\'mp2\'\>](/out/md/cml/orca_log/mp2-d3e22050.md)

Data source: [\<module cmlx:templateRef=\'ci\'\>](/out/md/cml/orca_log/ci-d3e22168.md)

Data source: [\<module cmlx:templateRef=\'dftd3\'\>](/out/md/cml/orca_log/dftd3-d3e22856.md)

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
