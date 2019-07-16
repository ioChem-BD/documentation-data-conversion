# Page components detail

# General Info

| Field                                                                                                                 | Source                                                                                                               | Sample value                                                                                                                                                  |
|----|----|----|
| Title                                                                                                                 | *Set on Browse calculation publication*                                                                              | Sample calculation                                                                                                                                            |
| Browse Item                                                                                                           | *URL pointing Browse published item*                                                                                 | https://iochem-bd.iciq.es/browse/handle/100/5672                                                                                                              |
| Program                                                                                                               | [header template](/out/md/cml/mopac_log/header-d3e35088.md)                                                                                  | Mopac 2016 - 16.041 64BITS                                                                                                                                    |
| Author                                                                                                                | *Username fullname*                                                                                                  | Alvarez Moreno, Moises                                                                                                                                        |
| Formula                                                                                                               | *Atom count from final geometry*                                                                                     | C 4 H 6 O 4                                                                                                                                                   |
| Calculation type                                                                                                      | Custom logic                                                                                                         | Geometry optimization                                                                                                                                         |
| Method                                                                                                                | Custom logic                                                                                                         | RASSCF RASPT2                                                                                                                                                 |

######Mopac - General Info - Main fields

![](/imgs/MOPAC_header.png)

[^1]

[^2]

# Molecular Info

This section captures molecule additional information not captured on previous section.

## Molecular Info

| Field                                                                                                                              | Source                                                                                                                             | Sample value                                                                                                                       |
|----|----|----|
| Charge                                                                                                                             | Readed from input file section of [input.file](/out/md/cml/mopac_log/input.file-d3e35135.md) module                                                        | 0.000                                                                                                                              |
| Multiplicity                                                                                                                       | Readed from input file section [input.file](/out/md/cml/mopac_log/input.file-d3e35135.md) module with SINGLET, DOUBLE, TRIPLET ... keywords.               | 3                                                                                                                                  |

######Molecular Info - Main fields

![](/imgs/MOPAC_molecularinfo.png)

# Atomic coordinates

After header section, our HTML resume will output a xyz coordinates table with current molecule atoms.

For every atom, we will output it's serial number, atom type, coordinates in angstroms.

Initially its readed from [geometry module](/out/md/cml/mopac_log/geometry-d3e35338.md)

![](/imgs/MOPAC_geometry.png)

# Modules

## IR spectrum / Vibrational frequencies

This module will display JSpecView + JSmol plugins (using javascript libraries) working together to represent molecule IR spectrum.

Data source: [&lt;module cmlx:templateRef='vibrations'&gt;](/out/md/cml/mopac_log/vibrations-d3e35039.md)

![](/imgs/ORCA_module_irspectrum.png)

## Final results - energies

Data source: [&lt;module cmlx:templateRef='energies'&gt;](/out/md/cml/mopac_log/energies-d3e35473.md)

![](/imgs/MOPAC_module_finalresults.png)

[^1]: string `molcas:getCalcType` boolean `isRestrictedOpt` boolean `isOptimization` boolean `isTS` boolean `isIncomplete`

    ```xml
        
        $isOptimization   Exists module <module cmlx:templateRef="optimization" > ?
        $hasVibrations    Exists module <module cmlx:templateRef="vibrations" > ?
         
        $negativeFrequenciesCount  Negative frequencies count from <module cmlx:templateRef="vibrations" > module
        $isTS                      A TS calculation was setup on the <module cmlx:templateRef="inputlines" >                             
                   
          <xsl:param name="isOptimization" as="xs:boolean"/>
            <xsl:param name="hasVibrations" as="xs:boolean"/>
            <xsl:param name="negativeFrequenciesCount" as="xs:integer"/>
            <xsl:param name="isTS" as="xs:boolean"/>
            
            <xsl:variable name="type">
                <xsl:choose>
                    <xsl:when test="$isOptimization">
                        <xsl:value-of select="$mp:GeometryOptimization"/>
                    </xsl:when>
                    <xsl:otherwise>
                        <xsl:value-of select="$mp:SinglePoint"/>
                    </xsl:otherwise>
                </xsl:choose>     
            </xsl:variable>
            
            <xsl:variable name="type2">
                <xsl:if test="$hasVibrations">
                    <xsl:choose>
                        <xsl:when test="$negativeFrequenciesCount = 1 and $isTS" >
                            <xsl:value-of select="$mp:TransitionState"/>
                        </xsl:when>
                        <xsl:when test="$negativeFrequenciesCount = 0">
                            <xsl:value-of select="$mp:Minimum"/>
                        </xsl:when >
                    </xsl:choose>
                </xsl:if>        
            </xsl:variable>        
            <xsl:value-of select="concat($type, ' ', $type2)"/>        
                            
                            
    ```

[^2]: string\* `mp:getMethods` nodes `inputLines`

    ```xml
        
        $inputLines   Input lines from <module cmlx:templateRef="inputlines" >                   
                      
        <xsl:variable name="mp:methodsRegex" select="'^(HF|UHF|RHF|PM3|PM6|PM6-D3|PM6-DH\+|PM6-DH2|PM6-DH2X|PM6-D3H4|PM6-D3H4X|PMEP|PM7|PM7-TS|AM1|RM1|MNDO|MNDOD).*'"/>
        
        <xsl:for-each select="$inputLines//cml:scalar[@dictRef='mp:inputline']">
            <xsl:variable name="line" select="./text()"/>        
            <xsl:for-each select="tokenize($line,'\s+')">
                <xsl:variable name="command" select="."/>
                    <xsl:if test="matches(upper-case($command), $mp:methodsRegex)">
                        <xsl:value-of select="$command"/><xsl:text> </xsl:text>
                    </xsl:if>
            </xsl:for-each>
        </xsl:for-each>
                            
                            
    ```
