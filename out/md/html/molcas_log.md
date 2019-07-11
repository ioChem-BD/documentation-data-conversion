# Page components detail

# General Info

| Field                                                                                   | Source                                                                                 | Sample value                                                                                                          |
|----|----|----|
| Title                                                                                   | *Set on Browse calculation publication*                                                | Sample calculation                                                                                                    |
| Browse Item                                                                             | *URL pointing Browse published item*                                                   | https://rodi.urv.es:8080/browse/handle/123456789/6                                                                    |
| Program                                                                                 | [program.header template](/out/md/cml/molcas_log/module.header-d3e28306.md)                                     | Molcas 8.0 - service pack 1                                                                                           |
| Author                                                                                  | *Username fullname*                                                                    | Alvarez Moreno, Moises                                                                                                |
| Formula                                                                                 | *Atom count from final geometry*                                                       | C 8 H 12 N 8 O 2                                                                                                      |
| Calculation type                                                                        | Custom logic                                                                           | Geometry optimization                                                                                                 |
| Method                                                                                  | Custom logic                                                                           | RASSCF RASPT2                                                                                                         |

######Molcas - General Info - Main fields

![](/imgs/MOLCAS_header.png)

[^1]

[^2]

# Atomics and Basis Sets

After header section, our HTML resume will output a xyz coordinates table with current molecule atoms.

For every atom, we will output it\'s serial number, atom type, coordinates in angstroms, basis used and contraction.

In geometry optimizations calculations, next to geometry section header there will appear the word **(optimized)**, pointing that this geometry is the last one from all optimization steps and has converged.

If the geometry optimization did not converge, there will appear the phrase **(calculation did not converge)**.

![](/imgs/MOLCAS_geometry.png)

# Molecular Info

This section captures molecule additional information not captured on previous section.

## Symmetry information

Data source: [\<module cmlx:templateRef=\'symmetry\'\>](/out/md/cml/molcas_log/symmetry-d3e31119.md)

![](/imgs/MOLCAS_symmetry.png)

## Molecular Info

| Field                                                                                             | Source                                                                                            | Sample value                                                                                      |
|----|----|----|
| Charge                                                                                            | Readed from \"charge\" scalar on [molcharge](/out/md/cml/molcas_log/molcharge.md) line or from                             | 0.000                                                                                             |
|                                                                                                   | [mulliken](/out/md/cml/molcas_log/mulliken-d3e30777.md) module                                                             |                                                                                                   |
| Multiplicity                                                                                      | Readed from scalar\[m:spinquantumnum\] inside [wave.specs](/out/md/cml/molcas_log/wave.specs-d3e28870.md) module OR from   | 3                                                                                                 |
|                                                                                                   | scalar\[m:spin\] inside [scf-ksdft](/out/md/cml/molcas_log/scf-ksdft-d3e30161.md) module                                   |                                                                                                   |

######Molecular Info - Main fields

![](/imgs/MOLCAS_molecularinfo.png)

## Solvation input

Data source: [\<module cmlx:templateRef=\'pcm\'\>](/out/md/cml/molcas_log/pcm-d3e28972.md)

Data source: [\<module cmlx:templateRef=\'kirkwood\'\>](/out/md/cml/molcas_log/kirkwood-d3e29027.md)

![](/imgs/MOLCAS_solvation.png)

## Integrals

Data source: [\<module cmlx:templateRef=\'seward.generate\'\>](/out/md/cml/molcas_log/seward.generate-d3e29078.md)

![](/imgs/MOLCAS_sewardgenerate.png)

## Bond distances

Data source (to read molecule and calculate bonds): [\<module cmlx:templateRef=\'coordinates\'\>](/out/md/cml/molcas_log/coordinates-d3e28646.md)

![](/imgs/MOLCAS_bonddistances.png)

## Restrictions in the Geometry Optimization

Data source: [\<module cmlx:templateRef=\'constraint\'\>](/out/md/cml/molcas_log/constraint-d3e32605.md)

![](/imgs/MOLCAS_restrictions.png)

# Modules

## Wave function specification

Data source: [\<module cmlx:templateRef=\'wave.specs\'\>](/out/md/cml/molcas_log/wave.specs-d3e28870.md)

![](/imgs/MOLCAS_module_wavefunction.png)

## Orbital specifications

Data source: [\<module cmlx:templateRef=\'orbital.specs\'\>](/out/md/cml/molcas_log/orbital.specs-d3e30246.md)

![](/imgs/MOLCAS_module_orbitalspecs.png)

## CI expansion specifications

Data source: [\<module cmlx:templateRef=\'ci.expansion\'\>](/out/md/cml/molcas_log/ci.expansion-d3e30526.md)

![](/imgs/MOLCAS_module_ciexpansion.png)

## Energies

Data source: [\<module cmlx:templateRef=\'wave.printout\'\>](/out/md/cml/molcas_log/wave.printout-d3e29140.md)

![](/imgs/MOLCAS_module_energies.png)

## Wave functions / Weights of the most important CSFs

Data source [\<module cmlx:templateRef=\'wave.printout\'\>](/out/md/cml/molcas_log/wave.printout-d3e29140.md)

![](/imgs/MOLCAS_module_wavefunctioncsf.png)

## Natural Occupation numbers

Data source: [\<module cmlx:templateRef=\'wave.printout\'\>](/out/md/cml/molcas_log/wave.printout-d3e29140.md), module \"natural\"

![](/imgs/MOLCAS_module_natural.png)

## Mulliken Spin Population

Data source: [\<module cmlx:templateRef=\'mulliken\'\>](/out/md/cml/molcas_log/mulliken-d3e30777.md), submodule \"mulliken.spin\"

![](/imgs/MOLCAS_module_mullikenspin.png)

## Electrostatic moments

Data source: [\<module cmlx:templateRef=\"properties\"\>](/out/md/cml/molcas_log/properties-d3e31233.md)

![](/imgs/MOLCAS_module_electrostaticmoments.png)

## Population analysis / Mulliken atomic charges

Data source: [\<module cmlx:templateRef=\"loprop\"\>](/out/md/cml/molcas_log/loprop-d3e31410.md)

Data source: [\<module cmlx:templateRef=\"mulliken\"\>](/out/md/cml/molcas_log/mulliken-d3e30777.md)

![](/imgs/MOLCAS_module_loprop.png)

![](/imgs/MOLCAS_module_mulliken.png)

## Single-State CASPT2

Data source: [\<module cmlx:templateRef=\"final.caspt2\"\>](/out/md/cml/molcas_log/final.caspt2-d3e31943.md)

![](/imgs/MOLCAS_module_singlestate_caspt2.png)

## Final energy

Data source: [\<module cmlx:templateRef=\"scf-ksdft\"\>](/out/md/cml/molcas_log/scf-ksdft-d3e30161.md) scalar dictRef=\'m:scfener\'

Data source: [\<module cmlx:templateRef=\"cchc\"\>](/out/md/cml/molcas_log/cchc-d3e32832.md) scalar dictRef=\'m:e2mp2energy\'

Data source: [\<module cmlx:templateRef=\"cchc\"\>](/out/md/cml/molcas_log/cchc-d3e32832.md) scalar dictRef=\'m:e2ccsdenergy\'

Data source: [\<module cmlx:templateRef=\"ccsdt\"\>](/out/md/cml/molcas_log/ccsdt.md) scalar dictRef=\'m:ccsdtcorrenergy\'

![](/imgs/MOLCAS_module_finalenergy.png)

![](/imgs/MOLCAS_module_finalenergy2.png)

## HZERO

Data source: [\<module cmlx:templateRef=\"extras\"\>](/out/md/cml/molcas_log/extras-d3e31478.md)

![](/imgs/MOLCAS_module_hzero.png)

## Harmonic frequencies

This module also allows displaying harmonic frequency intensities on a customizable chart.

Data source: [\<module cmlx:templateRef=\'vibrations\'\>](/out/md/cml/molcas_log/vibrations-d3e32468.md)

![](/imgs/MOLCAS_module_harmonicfreq.png)

![](/imgs/MOLCAS_module_harmonicfreq2.png)

## IR spectrum / Vibrational frequencies

Data source: [\<module cmlx:templateRef=\'vibrations\'\>](/out/md/cml/molcas_log/vibrations-d3e32468.md)

This module will display JSpecView + JSmol plugins (using javascript libraries) working together to represent molecule IR spectrum.

![](/imgs/MOLCAS_module_frequencies.png)

## Multipole Expansion Analysis

Data source:[\<module cmlx:templateRef=\"atom.expansion\"\>](/out/md/cml/molcas_log/atom.expansion-d3e32908.md)

![](/imgs/MOLCAS_module_multipoleexpansion.png)

## LoProp Analysis

Data source: [\<module cmlx:templateRef=\'dynamic.loprop\'\>](/out/md/cml/molcas_log/dynamic.loprop-d3e33034.md)

![](/imgs/MOLCAS_module_loprop_analysis.png)

[^1]: string `molcas:getCalcType` boolean `isRestrictedOpt` boolean `isOptimization` boolean `isTS` boolean `isIncomplete`

    ```xml
                                
        $isRestrictedOpt  Exists module <module cmlx:templateRef="constraint" > ?
        $isOptimization   Input file from <module cmlx:templateRef="molcas.input" > is setup to perform a geometry optimization? 
        $isTS           TS keyword is defined inside <module cmlx:templateRef="molcas.input" > ?
        $isIncomplete   Convergence table from <module cmlx:templateRef="energy.statistics" > shows 'all converged' OR $isOptimization and $hasLastEnergySection ?                             
                   
        
        <!-- Calculation type related constants -->
        <xsl:param name="isRestrictedOpt"/>
        <xsl:param name="isOptimization"/>
        <xsl:param name="isTS"/>
        <xsl:param name="isIncomplete"/>

        <xsl:choose>
            <xsl:when test="$isRestrictedOpt">
                <xsl:value-of select="$molcas:RestrictedGeomOpt"/>
            </xsl:when>
            <xsl:when test="$isOptimization">
                <xsl:value-of select="$molcas:GeometryOpt"/>
            </xsl:when>
            <xsl:otherwise>
                <xsl:value-of select="$molcas:SinglePoint"/>    
            </xsl:otherwise>            
        </xsl:choose>
        <xsl:if test="$isTS">
            <xsl:text> </xsl:text><xsl:value-of select="$molcas:TS"/>
        </xsl:if>               
        <xsl:if test="$isIncomplete">
            <xsl:text> </xsl:text><xsl:value-of select="$molcas:Incomplete"/>
        </xsl:if>                           
                            
                            
    ```

[^2]: string `molcas:getMethods` node\* `modules` node `ksdft` node `wavespecs`

    ```xml
                                
        $modules    Array with all executed module names 
        $ksdft      Module from <module cmlx:templateRef="scf-ksdft" > 
        $wavespecs  Entire <module cmlx:templateRef="wave.specs" > module                             
                   
        
            <xsl:param name="modules"/>
            <xsl:param name="ksdft" />
            <xsl:param name="wavespecs" />

            <xsl:variable name="isCASSCF" select="
                if(exists($wavespecs) and contains($modules,$molcas:RASSCFmodule) and ($wavespecs/cml:scalar[@dictRef='m:ras1holes'] = '0') and ($wavespecs/cml:scalar[@dictRef='m:ras3holes'] = 0)) then
                    true()                
                else
                    false()"/>
            <xsl:variable name="isRASSCF" select="
                if(contains($modules,$molcas:RASSCFmodule)) then
                    true()
                else
                    false()"/>      
            
            <xsl:variable name="moduleArray">
                <xsl:for-each select="$modules">                
                    <xsl:value-of select="concat(upper-case(string(.)),'|')"/>
                </xsl:for-each>
            </xsl:variable>
            
            <xsl:for-each select="distinct-values(tokenize($moduleArray/text(),'[|]+'))">
                <xsl:if test="matches(.,$molcas:methodsRegex)">
                    <xsl:choose>
                        <xsl:when test="exists($ksdft) and matches(.,$molcas:SCFmodule)">
                            <xsl:choose>
                                <xsl:when test="matches($ksdft,$molcas:SCFmodule)">
                                    <xsl:text>HF </xsl:text>
                                </xsl:when>
                                <xsl:otherwise>
                                    <xsl:text>DFT </xsl:text>
                                </xsl:otherwise>
                            </xsl:choose>
                        </xsl:when>
                        <xsl:when test="matches(.,$molcas:RASSCFmodule)">                        
                            <xsl:choose>
                                <xsl:when test="$isCASSCF">
                                    <xsl:value-of select="$molcas:CASSCFmodule"/><xsl:text> </xsl:text>
                                </xsl:when>
                                <xsl:otherwise>
                                    <xsl:value-of select="."/><xsl:text> </xsl:text>
                                </xsl:otherwise>
                            </xsl:choose>
                        </xsl:when>
                        <xsl:when test="matches(.,$molcas:CASPT2module)">
                            <xsl:choose>
                                <xsl:when test="not($isCASSCF) and $isRASSCF">
                                    <xsl:value-of select="$molcas:RASPT2module"/><xsl:text> </xsl:text>
                                </xsl:when>
                                <xsl:otherwise>
                                    <xsl:value-of select="."/><xsl:text> </xsl:text>
                                </xsl:otherwise>
                            </xsl:choose>
                        </xsl:when>
                        <xsl:otherwise>
                            <xsl:value-of select="."/><xsl:text> </xsl:text>
                        </xsl:otherwise>
                    </xsl:choose>
                </xsl:if>           
            </xsl:for-each>              
                            
                            
    ```
