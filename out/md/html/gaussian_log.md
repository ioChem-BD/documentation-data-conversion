# Page components detail

# General Info

| Field                                                                                                                 | Source                                                                                                               | Sample value                                                                                                                                                  |
|----|----|----|
| Title                                                                                                                 | *Set on Browse calculation publication*                                                                              | Sample calculation                                                                                                                                            |
| Browse Item                                                                                                           | *URL pointing Browse published item*                                                                                 | https://iochem-bd.iciq.es/browse/handle/100/1722                                                                                                              |
| Program                                                                                                               | [&lt;scalar dictRef="cc:program"&gt;](#jobcpu-d3e17433) - [&lt;scalar dictRef="cc:program"&gt;](/out/md/cml/gaussian_log/l1.end-d3e5926.md)     | Gaussian 09                                                                                                                                                   |
|                                                                                                                       | template                                                                                                             |                                                                                                                                                               |
| Author                                                                                                                | *Username fullname*                                                                                                  | Alvarez Moreno, Moises                                                                                                                                        |
| Formula                                                                                                               | *Atom count from final geometry*                                                                                     | H 1 O 40 P 1 Ti 1 W 11                                                                                                                                        |
| Calculation type                                                                                                      | Custom logic                                                                                                         | Geometry optimization Minimum                                                                                                                                 |
| Method                                                                                                                | DFT                                                                                                                  | DFT                                                                                                                                                           |

######Gaussian - General Info - Main fields

| Field                                                                                                                              | Source                                                                                                                             | Sample value                                                                                                                       |
|----|----|----|
| Temperature                                                                                                                        | [&lt;scalar dictRef="cc:temp"&gt;](/out/md/cml/gaussian_log/l716.thermochemistry.temperature-d3e14601.md)                                                     | 298.15 K                                                                                                                           |
| Pressure                                                                                                                           | [&lt;scalar dictRef="cc:press"&gt;](/out/md/cml/gaussian_log/l716.thermochemistry.temperature-d3e14601.md)                                                    | 1.0 atm                                                                                                                            |

######Gaussian - General Info with additional fields (if [thermochemistry](/out/md/cml/gaussian_log/l716.thermochemistry-d3e14592.md) module exists)

![](/imgs/GAUSSIAN_header.png)

![](/imgs/GAUSSIAN_header2.png)

[^1]

# Atoms and Basis Sets

After header section, our HTML resume will output a xyz coordinates table with current molecule atoms.

For every atom, we will output it's serial number, atom type, coordinates in angstroms, [basis used and core](#l301.basis2-d3e11876), or simply [basis](/out/md/cml/gaussian_log/l301.basis-d3e11588.md).

In geometry optimizations calculations, next to geometry section header there will appear the word **(optimized)**, pointing that this geometry is the last one from all optimization steps and has converged.

If the geometry optimization did not converge, there will appear the phrase **(calculation did not converge)**.

If there are multiple geometries we'll capture it's last appearance.

![](/imgs/GAUSSIAN_geometry.png)

![](/imgs/GAUSSIAN_geometry2.png)

![](/imgs/GAUSSIAN_geometry3.png)

# Molecular Info

This section captures molecule additional information not captured on previous section.

| Field                                                                                                                              | Source                                                                                                                             | Description                                                                                                                        |
|----|----|----|
| Multiplicity                                                                                                                       | Appears in                                                                                                                         |                                                                                                                                    |
|                                                                                                                                    |                                                                                                                                    |                                                                                                                                    |
|                                                                                                                                    | -   qmm module [&lt;array dictRef="g:multiplicity"&gt;](/out/md/cml/gaussian_log/l101.qmmm-d3e6285.md)                                                        |                                                                                                                                    |
|                                                                                                                                    |                                                                                                                                    |                                                                                                                                    |
|                                                                                                                                    | -   [l101.zmat module](/out/md/cml/gaussian_log/l101.zmat-d3e6758.md)                                                                                         |                                                                                                                                    |
|                                                                                                                                    |                                                                                                                                    |                                                                                                                                    |
|                                                                                                                                    | -   [l101.zmata module](/out/md/cml/gaussian_log/l101.zmata-d3e6840.md)                                                                                       |                                                                                                                                    |
|                                                                                                                                    |                                                                                                                                    |                                                                                                                                    |
|                                                                                                                                    | -   l9999.archive module [&lt;scalar @dictRef='x:spinMultiplicity'&gt;](/out/md/cml/gaussian_log/l9999.archive-d3e16761.md)                                   |                                                                                                                                    |
| Charge                                                                                                                             | It can appear on same places that multiplicity field and also in [l9999.archive module](/out/md/cml/gaussian_log/l9999.archive-d3e16761.md)                   |                                                                                                                                    |
| QMMM                                                                                                                               | [&lt;module cmlx:templateRef="l101.qmmm"&gt;](/out/md/cml/gaussian_log/l101.qmmm-d3e6285.md)                                                                  |                                                                                                                                    |
| Frozen section                                                                                                                     | [&lt;module cmlx:templateRef="l101.modredundant"&gt;](/out/md/cml/gaussian_log/l101.modredundant-d3e7221.md)                                                  |                                                                                                                                    |
| Point group                                                                                                                        | [&lt;module cmlx:templateRef="l202.stoich"&gt;](/out/md/cml/gaussian_log/l202.stoich-d3e11494.md)                                                             |                                                                                                                                    |
| Solvation                                                                                                                          | [&lt;module cmlx:templateRef="l301.pcm.standard"&gt;](/out/md/cml/gaussian_log/l301.pcm.standard-d3e12638.md)                                                 | Solvation parameters                                                                                                               |

######Molecular Info - Main fields

![](/imgs/GAUSSIAN_molecularinfo.png)

![](/imgs/GAUSSIAN_molecularinfo2.png)

# Modules

## Energies

Data source: [&lt;scalar dictRef='g:rbhflyp'&gt;](/out/md/cml/gaussian_log/l502.footer-d3e13408.md)

Data source: [&lt;scalar dictRef='cc:dispenergy'&gt;](/out/md/cml/gaussian_log/l502.pcm-d3e13547.md)

Data source: [&lt;module cmlx:templateRef='l120'&gt;](/out/md/cml/gaussian_log/l120-d3e11231.md)

Data source: [&lt;module cmlx:templateRef='l122'&gt;](/out/md/cml/gaussian_log/l122-d3e16546.md)

Data source: [&lt;module cmlx:templateRef='l716.zeropoint'&gt;](/out/md/cml/gaussian_log/l716.zeropoint-d3e14279.md)

Data source: [&lt;module cmlx:templateRef='l9999.archive'&gt;](/out/md/cml/gaussian_log/l9999.archive-d3e16761.md)

![](/imgs/GAUSSIAN_module_energies.png)

![](/imgs/GAUSSIAN_module_energies1.png)

## Spin

Data source: [&lt;module cmlx:templateRef='l601.mullikenspin'&gt;](/out/md/cml/gaussian_log/l601.mullikenspin-d3e9226.md)

Data source: [&lt;scalar dictRef='cc:spincontamination'&gt;](/out/md/cml/gaussian_log/l502.footer2-d3e13587.md)

![](/imgs/GAUSSIAN_module_l601_mullikenspin.png)

## IR spectrum

Data source: [&lt;module cmlx:templateRef='l716.freq.chunkx'&gt;](/out/md/cml/gaussian_log/l716.freq.chunkx-d3e13919.md)

This module will display JSpecView + JSmol plugins (using javascript libraries) working together to represent molecule IR spectrum.

![](/imgs/GAUSSIAN_module_frequencies.png)

## Mulliken atomic charges

Data source: [&lt;module cmlx:templateRef='mulliken'&gt;](/out/md/cml/gaussian_log/mulliken-d3e9187.md)

![](/imgs/GAUSSIAN_module_mulliken.png)

## Dipole / Multipole moment

Data source: [&lt;module cmlx:templateRef="multipole"&gt;](/out/md/cml/gaussian_log/multipole-d3e9353.md)

![](/imgs/GAUSSIAN_module_dipole_moment.png)

[^1]: string `gaussian:getCalcType` boolean `isOptimization` boolean `hasStationaryPoint` boolean `hasMinimum`

    ```xml
                                    
        $isOptimization       Exists module <module cmlx:templateRef="l103" > ?
        $hasStationaryPoiny   'Stationary point found' appears in <module cmlx:templateRef="l103.optimizedparam" > ?
        $hasMinimum           'Search for a local minimum' appears in <module cmlx:templateRef="l103.localminsaddle" > ?                               
                   
        
        <!-- Calculation type related constants -->
        <xsl:variable name="calcType" select="if($isOptimization) then 'Geometry optimization' else 'Single point'"/>       
            <xsl:choose>
                <xsl:when test="$hasStationaryPoint">
                    <xsl:variable name="hasMinimum" select="if($hasMinimum) then ' Minimum' else ' TS'"/>
                    <xsl:sequence select="concat($calcType, ' ' , $hasMinimum)"/>
                </xsl:when>
                <xsl:otherwise>
                    <xsl:sequence select="concat($calcType, ' Structure')"/>
                </xsl:otherwise>
            </xsl:choose>                          
         
                            
    ```
