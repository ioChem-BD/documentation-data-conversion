# Page components detail

# Header

| Field                                                                                                                 | Source                                                                                                               | Sample value                                                                                                                                                  |
|----|----|----|
| Title                                                                                                                 | *Set on Browse calculation publication*                                                                              | Sample calculation                                                                                                                                            |
| Browse Item                                                                                                           | *URL pointing Browse published item*                                                                                 | https://iochem-bd.iciq.es/browse/handle/100/1722                                                                                                              |
| Program                                                                                                               | [&lt;scalar dictRef="cc:program"&gt;](/out/md/cml/turbomole_log/program-d3e23383.md) template                                                    | Turbomole 5.3.2                                                                                                                                               |
| Author                                                                                                                | *Username fullname*                                                                                                  | Alvarez Moreno, Moises                                                                                                                                        |
| Formula                                                                                                               | *Atom count from final geometry*                                                                                     | C 6 H 12 Fe 1 N 24                                                                                                                                            |
| Calculation type                                                                                                      | Custom logic                                                                                                         | Geometry optimization Minimum                                                                                                                                 |
| Method(s)                                                                                                             | Custom logic                                                                                                         | DFT (b3-lyp, D3, ri-j, gridsize:m3)                                                                                                                           |

######Turbomole - General Info - Main fields

![](/imgs/TURBOMOLE_header.png)

[^1]

[^2]

# Atoms and Basis Sets

After header section, our HTML resume will output a xyz coordinates table with current molecule atoms.

Initially its readed from [coord file](/out/md/cml/turbomole_log/turbomole.coord-d3e36704.md)

Then we will read all instances from module [&lt;module cmlx:templateRef="atomcoord"&gt;](/out/md/cml/turbomole_log/atomcoord-d3e23579.md) and use last instance as final geometry

For every atom, we will output it's serial number, atom type, coordinates in angstroms, and [basis used](/out/md/cml/turbomole_log/basisset-d3e24211.md).

In geometry optimizations calculations, next to geometry section header there will appear the word **(optimized)**, pointing that this geometry is the last one from all optimization steps and has converged.

If the geometry optimization [did not converge](/out/md/cml/turbomole_log/convergence.info-d3e25992.md), there will appear the phrase **(calculation did not converge)**.

If there are multiple geometries we'll capture it's last appearance.

![](/imgs/TURBOMOLE_geometry.png)

# Molecular Info

This section captures molecule additional information not captured on previous section.

| Field                                                                                                                              | Source                                                                                                                             | Description                                                                                                                        |
|----|----|----|
| Symmetry                                                                                                                           | Appears in [symmetry module](/out/md/cml/turbomole_log/symmetry-d3e24268.md).                                                                                  | Symmetry information about the molecule (if it exists)                                                                             |
| Multiplicity                                                                                                                       | Its value is set:                                                                                                                  |                                                                                                                                    |
|                                                                                                                                    |                                                                                                                                    |                                                                                                                                    |
|                                                                                                                                    | -   Set to 1 on closed shell calculations                                                                                          |                                                                                                                                    |
|                                                                                                                                    |                                                                                                                                    |                                                                                                                                    |
|                                                                                                                                    | -   On open shell calculations = alpha - beta electrons on occupied orbitals                                                       |                                                                                                                                    |
| Charge                                                                                                                             | Readed from:                                                                                                                       |                                                                                                                                    |
|                                                                                                                                    |                                                                                                                                    |                                                                                                                                    |
|                                                                                                                                    | -   [&lt;scalar @dictRef='t:charge'&gt;](/out/md/cml/turbomole_log/electrostatic.moments-d3e25300.md)                                                          |                                                                                                                                    |
|                                                                                                                                    |                                                                                                                                    |                                                                                                                                    |
|                                                                                                                                    | -   On closed shell calculations = atomic charge - electronic\_charge \* 2 ([Orbital statistics                                    |                                                                                                                                    |
|                                                                                                                                    |     module](#molecular.orbitals.statistics-d3e25913))                                                                              |                                                                                                                                    |
|                                                                                                                                    |                                                                                                                                    |                                                                                                                                    |
|                                                                                                                                    | -   On open shell calculations = atomic charge - (alpha electrons + beta electrons) ([Unrestricted orbitals control file           |                                                                                                                                    |
|                                                                                                                                    |     section](#unrestrictedorbitals-d3e36634))                                                                                      |                                                                                                                                    |
| Geometry restrictions                                                                                                              | [&lt;module cmlx:templateRef="restrictions"&gt;](/out/md/cml/turbomole_log/restrictions-d3e37057.md)                                                           | User defined geometry restrictions                                                                                                 |
| Solvation                                                                                                                          | [&lt;module cmlx:templateRef="cosmo"&gt;](/out/md/cml/turbomole_log/cosmo-d3e24713.md)                                                                         | Solvation parameters                                                                                                               |

######Molecular Info - Main fields

![](/imgs/TURBOMOLE_molecularinfo.png)

# Modules

## Population analysis

Data source: [&lt;module cmlx:templateRef='population.analysis'&gt;](/out/md/cml/turbomole_log/population.analysis-d3e23974.md)

Data source: [&lt;module cmlx:templateRef='fit.pointcharges'&gt;](/out/md/cml/turbomole_log/fit.pointcharges-d3e26303.md)

This module will hold Mulliken, Loewdin and Natural population analysis, will also contain (if exists) information from unpaired electrons from D(alpha)-D(beta)

![](/imgs/TURBOMOLE_module_popanalysis.png)

## Electrostatic moments

Data source: [&lt;module cmlx:templateRef='electrostatic.moments'&gt;](/out/md/cml/turbomole_log/electrostatic.moments-d3e25300.md)

This module will display charge, dipole and multipole values.

![](/imgs/TURBOMOLE_module_electromoments.png)

## Orbital specification

Data source: [&lt;module cmlx:templateRef='orbitals'&gt;](/out/md/cml/turbomole_log/orbitals-d3e24347.md)

![](/imgs/TURBOMOLE_module_orbspecification.png)

## Final results

Data source: [&lt;module cmlx:templateRef='turbomole.energy'&gt;](/out/md/cml/turbomole_log/turbomole.energy-d3e39658.md) Taken from last line of energy file

Data source: [&lt;module cmlx:templateRef='energy'&gt;](/out/md/cml/turbomole_log/energy-d3e26177.md)

Data source: [&lt;module cmlx:templateRef='nuclear.repulsion'&gt;](/out/md/cml/turbomole_log/nuclear.repulsion-d3e26143.md)

Data source: [&lt;module cmlx:templateRef='zero.point.energy'&gt;](/out/md/cml/turbomole_log/zero.point.energy-d3e26276.md)

![](/imgs/TURBOMOLE_module_finalresults.png)

## IR spectrum

Data source: [&lt;module cmlx:templateRef='vibrations'&gt;](/out/md/cml/turbomole_log/vibrations-d3e36296.md)

This module will display JSpecView + JSmol plugins (using javascript libraries) working together to represent molecule IR spectrum.

All information will come from "\$vibrational normal modes" and "\$vibrational spectrum" sections inside Turbomole *control* file, in case they are defined on external files such as *vib\_normal\_modes* and *vibspectrum*we must copy them inside *control* file.

![](/imgs/TURBOMOLE_module_irspectrum.png)

## TDDFT/TDHF

Data source: [&lt;module cmlx:templateRef='excitation'&gt;](/out/md/cml/turbomole_log/excitation-d3e24425.md)

![](/imgs/TURBOMOLE_module_tddft1.png)

[^1]: string `turbo:getCalcType` boolean `isRestrictedOptimization` boolean `isOptimization` boolean `isIncomplete` nodeset `vibrations` nodeset `statpt` nodeset `soes`

```xml
        $isRestrictedOptimization       Exists module <module cmlx:templateRef="restrictions" > ?
        $isOptimization                 Exists module <module cmlx:templateRef="convergence.info" > ?
        $isIncomplete                   Last module <module cmlx:templateRef="convergence.info" > has a "NO" on converged fields?   
        $vibrations                     Vibrational frequencies information, headers and displacements. Refer to <module cmlx:templateRef="vibrations" > 
        $statpt                         statpt parameters section readed from control file
        $soes                           soes parameters section readed from control file
                   
            <xsl:param name="isRestrictedOptimization" as="xs:boolean"/>
            <xsl:param name="isOptimization" as="xs:boolean"/>
            <xsl:param name="isIncomplete" as="xs:boolean"/>
            <xsl:param name="vibrations" as="node()?"/>
            <xsl:param name="statpt" as="node()?"/>
            <xsl:param name="soes" as="node()?"/>
            
            <xsl:variable name="isMinimum" select="not(contains(replace($vibrations/cml:module[@cmlx:templateRef='spectrum']/array[@dictRef='cc:frequency'],'-0.00',''), '-'))"/>
            <xsl:variable name="isExcitedState">           
                <xsl:if test="exists($soes) and number($soes/cml:array[@dictRef='t:irrep']/@size) = 1">
                    <xsl:value-of select="$turbo:ExcitedState"/>
                    <xsl:text> </xsl:text>
                    <xsl:if test="$isRestrictedOptimization or $isOptimization">
                        (<xsl:value-of select="$soes/cml:array[@dictRef='t:lowest']"/><xsl:value-of select="$soes/cml:array[@dictRef='t:irrep']"/>)    
                    </xsl:if>                                
                </xsl:if>              
            </xsl:variable>
            
            <xsl:variable name="isTS" select="
                if(exists($statpt) and number($statpt//cml:scalar[@dictRef='t:itrvec']) > 0) then
                    $turbo:TransitionState
                else
                    ''
                "/>
            <xsl:variable name="itrvecdsd" select="number($statpt//cml:scalar[@dictRef='t:itrvec'])"/>
            <xsl:variable name="calcType" select="
                if($isRestrictedOptimization) then               
                    $turbo:RestrictedGeometryOptimization                 
                else if($isOptimization) then
                    concat($turbo:GeometryOptimization, ' ', $isTS)
                else 
                    $turbo:SinglePoint                
           "/>
            
            
            <xsl:variable name="vibration" select="
                if(exists($vibrations) and not($isRestrictedOptimization) and compare($isTS,'') = 0) then
                    if($isMinimum) then 
                        $turbo:Minimum
                    else
                        $turbo:TransitionState             
                else ''
            "/>
            <xsl:sequence select="concat($calcType, ' ', $vibration, ' ', $isExcitedState)"/>
         
                            
```

[^2]: string `turbo:getMehod` nodeset `soes` nodeset `methodScalar`

```xml
     
            $soes           soes parameters section readed from control file <module cmlx:templateRef="soes">  
            $methodScalar   methods readed from control file ($dft|$uhf)   <module cmlx:templateRef="methods">
                                
                                
            <xsl:variable name="methodsTmp">
                <xsl:for-each select="$methodScalar">
                    <xsl:for-each select="tokenize(.,'\s+')">
                        <xsl:element name="method">
                            <xsl:value-of select="upper-case(.)"/>
                            <xsl:text> </xsl:text>
                        </xsl:element>                    
                    </xsl:for-each>
                </xsl:for-each>
            </xsl:variable>
            <xsl:choose>            
                <xsl:when test="not(exists($methodScalar))">
                    <xsl:sequence select="                 
                        if(exists($soes)) then
                            'TDHF'
                        else
                            'HF'                                          
                        ">
                    </xsl:sequence>                
                </xsl:when>      
                <xsl:otherwise>
                    <xsl:variable name="step1">
                        <xsl:choose>
                            <xsl:when test="contains($methodsTmp, 'RIR12') and contains($methodsTmp, 'MP2') and contains($methodsTmp, 'RICC2')">
                                <xsl:text>MP2-F12 </xsl:text>
                                <xsl:value-of select="replace(replace(replace($methodsTmp,'RIR12', ''), 'MP2', ''), 'RICC2', '')"></xsl:value-of>
                            </xsl:when>
                            <xsl:otherwise><xsl:value-of select="$methodsTmp"/></xsl:otherwise>
                        </xsl:choose>           
                    </xsl:variable>
                    
                    <xsl:variable name="step2">
                        <xsl:choose>
                            <xsl:when test="contains($step1, 'UHF') and contains($step1, 'DFT')">
                                <xsl:text>U-DFT </xsl:text>
                                <xsl:value-of select="replace(replace($step1,'UHF',''), 'DFT','')"/>
                            </xsl:when>
                            <xsl:otherwise><xsl:value-of select="$step1"/></xsl:otherwise>
                        </xsl:choose>           
                    </xsl:variable>
                    
                    <xsl:variable name="step3">
                        <xsl:choose>
                            <xsl:when test="contains($step2, 'DFT') and exists($soes)">
                                <xsl:value-of select="replace($step2,'DFT', 'TDDFT')"/>
                            </xsl:when>
                            <xsl:otherwise><xsl:value-of select="$step2"/></xsl:otherwise>
                        </xsl:choose>               
                    </xsl:variable>
                    
                    <xsl:value-of select="$step3"/>                
                </xsl:otherwise>
            </xsl:choose>       
                                
                            
```
