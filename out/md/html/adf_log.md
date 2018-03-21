# Page components detail

# General Info

| Field                                                                                   | Source                                                                                 | Sample value                                                                                                          |
|----|----|----|
| Title                                                                                   | *Set on Browse calculation publication*                                                | Sample calculation                                                                                                    |
| Browse Item                                                                             | *URL pointing Browse published item*                                                   | https://argo.urv.es:8080/jspui/handle/123456789/6                                                                     |
| Program                                                                                 | [program.header template](/out/md/cml/adf_log/program.header-d3e26)                                       | ADF 2007                                                                                                              |
| Author                                                                                  | *Username fullname*                                                                    | Alvarez Moreno, Moises                                                                                                |
| Formula                                                                                 | *Atom count from final geometry*                                                       | H 1 O 40 P 1 Ti 1 W 11                                                                                                |
| Calculation type                                                                        | Custom logic                                                                           | Geometry optimization Minimum                                                                                         |
| Method                                                                                  | DFT                                                                                    | DFT                                                                                                                   |

######ADF - General Info - Main fields

| Field                                                                                             | Source                                                                                            | Sample value                                                                                      |
|----|----|----|
| Temperature                                                                                       | [&lt;scalar dictRef="cc:temp"&gt;](/out/md/cml/adf_log/thermochemistry-d3e3914)                                      | 300 K                                                                                             |
| Pressure                                                                                          | [&lt;scalar dictRef="cc:press"&gt;](/out/md/cml/adf_log/thermochemistry-d3e3914)                                     | 1.0 atm                                                                                           |

######ADF - General Info - Additional fields (if [thermochemistry](/out/md/cml/adf_log/thermochemistry-d3e3914) module exists)

![](/imgs/ADF_header.png)

[^1]

# Atoms and Basis Sets

After header section, our HTML resume will output a xyz coordinates table with current molecule atoms.

For every atom, we will output it's serial number, atom type, coordinates in angstroms, basis used and contraction.

In geometry optimizations calculations, next to geometry section header there will appear the word **(optimized)**, pointing that this geometry is the last one from all optimization steps and has converged.

If the geometry optimization did not converge, there will appear the phrase **(calculation did not converge)**.

If there are multiple geometries we'll capture them acording with the following table order :

| Section                                                                                                                                             | Note                                                                                                                                                |
|----|----|
| [&lt;module cmlx:templateRef="geometry.cycle"&gt;](/out/md/cml/adf_log/geometry.cycle-d3e2028)                                                                         | Latest geometry cycle(Coordinates on Input orientation)                                                                                             |
| [&lt;module cmlx:templateRef="geometry.cycle"&gt;](/out/md/cml/adf_log/geometry.cycle-d3e2028)                                                                         | Lastest geom.opt. (Coordinates)                                                                                                                     |
| [&lt;module cmlx:templateRef="quild.coord"&gt;](/out/md/cml/adf_log/quild.coord-d3e4161)                                                                               | Latest quild iteration                                                                                                                              |
| [&lt;module cmlx:templateRef="nuclear.coordinates"&gt;](/out/md/cml/adf_log/nuclear.coordinates-d3e145)                                                                | NMR geometry                                                                                                                                        |
| [&lt;module cmlx:templateRef="geometry"&gt;](/out/md/cml/adf_log/geometry-d3e1546)                                                                                     | Single point initial geometry                                                                                                                       |

######Atomic coordinates - Possible candidates (most important first)

![](/imgs/ADF_geometry.png)

# Molecular Info

This section captures molecule additional information not captured on previous section.

| Field                                                                                             | Source                                                                                            | Description                                                                                       |
|----|----|----|
| Spin polarization                                                                                 | [&lt;scalar dictRef="a:spinPolarization"&gt;](/out/md/cml/adf_log/logfile-d3e4294)                                   | Variable found inside logfile module (last instance is captured)                                  |
| Multiplicity                                                                                      | Depends on [spin polarization](/out/md/cml/adf_log/spinPolarization)                                                 | If spin polarization exists, multiplicity = spinpolarization + 1, otherwise multiplicity = 1      |
| Charge                                                                                            | [&lt;scalar dictRef="a:charge"&gt;](/out/md/cml/adf_log/logfile-d3e4294)                                             | Variable found inside logfile module (last instance is captured)                                  |
| Solvation                                                                                         | [&lt;module cmlx:templateRef="solvation"&gt;](/out/md/cml/adf_log/solvation-d3e1402)                                 | Solvation parameters                                                                              |

######Molecular Info - Main fields

![](/imgs/ADF_molecularinfo.png)

# Modules

## Bonding energy

Data source: [&lt;module cmlx:templateRef='bonding.energy'&gt;](/out/md/cml/adf_log/bonding.energy-d3e3015)

![](/imgs/ADF_module_bondingenergies.png)

## Fit test

Data source: [&lt;module cmlx:templateRef='fit.test'&gt;](/out/md/cml/adf_log/fit.test-d3e2555)

![](/imgs/ADF_module_fittest.png)

## MOs / SFO gross populations

Data source: [&lt;module cmlx:templateRef='molecular-orbitals'&gt;](/out/md/cml/adf_log/molecular.orbitals-d3e3125)

![](/imgs/ADF_module_molecularorbitals.png)

## MOs Energies

Data source: [&lt;module cmlx:templateRef='orbital.energies'&gt;](/out/md/cml/adf_log/orbital.energies-d3e2470)

Data source: [&lt;module cmlx:templateRef='orbital.energies.spin'&gt;](/out/md/cml/adf_log/orbital.energies.spin-d3e2511)

![](/imgs/ADF_module_orbitalenergies.png)

Data source: [&lt;module cmlx:templateRef='orbital.energies.spin'&gt;](/out/md/cml/adf_log/orbital.energies.spin-d3e2511)

![](/imgs/ADF_module_orbitalenergiesspin.png)

## Mulliken Atomic Charges

Data source [&lt;module cmlx:templateRef='mulliken'&gt;](/out/md/cml/adf_log/mulliken-d3e2608)

![](/imgs/ADF_module_mullikenatomiccharges.png)

## Multipole Derived Atomic Charges

Data source: [&lt;module cmlx:templateRef='atomic.charges'&gt;](/out/md/cml/adf_log/atomic.charges-d3e2805)

Data source: [&lt;module cmlx:templateRef='atomic.charges.spin'&gt;](/out/md/cml/adf_log/atomic.charges.spin-d3e2855)

Data source: [&lt;module cmlx:templateRef='spin.density'&gt;](/out/md/cml/adf_log/spin.density-d3e2905)

![](/imgs/ADF_module_multipolederivedatomiccharges.png)

![](/imgs/ADF_module_multipolederivedatomiccharges2.png)

![](/imgs/ADF_module_multipolederivedatomiccharges3.png)

## Quadrupole Moment

Data source: [&lt;module cmlx:templateRef='quadrupole.moment'&gt;](/out/md/cml/adf_log/quadrupole.moment-d3e2958)

![](/imgs/ADF_module_quadrupolemoment.png)

## S\*\*2

Data source: [&lt;module cmlx:templateRef="s2"&gt;](/out/md/cml/adf_log/s2-d3e2987)

![](/imgs/ADF_module_s2.png)

## Vibrational Frequencies and Intensities

Data source: [&lt;module cmlx:templateRef='intensities'&gt;](/out/md/cml/adf_log/intensities-d3e3875)

![](/imgs/ADF_module_intensities.png)

## IR spectrum

Data source: [&lt;module cmlx:templateRef='vibrations'&gt;](/out/md/cml/adf_log/vibrations-d3e3797)

This module will display JSpecView + JSmol plugins (using javascript libraries) working together to represent molecule IR spectrum.

![](/imgs/ADF_module_frequencies.png)

## Zero Point Energy

Data source:

-   [&lt;module cmlx:templateRef="zeropoint"&gt;&lt;scalar dictRef="cc:zeropoint"&gt;](/out/md/cml/adf_log/zeropoint-d3e3766)

![](/imgs/ADF_module_zeropointenergy.png)

## Thermochemistry

Data source: [&lt;module cmlx:templateRef='thermochemistry'&gt;](/out/md/cml/adf_log/thermochemistry-d3e3914)

![](/imgs/ADF_module_thermochemistry.png)

## Final Excitation Energies

Data source: [&lt;module cmlx:templateRef='excitation.energy'&gt;](/out/md/cml/adf_log/excitation.energy-d3e3539)

![](/imgs/ADF_module_finalexcitationenergies.png)

## NMR Shielding Tensors

Data source: [&lt;module cmlx:templateRef='nmr'&gt;](/out/md/cml/adf_log/nmr-d3e19)

![](/imgs/ADF_module_nmr.png)

## Timing

Data source: [&lt;module cmlx:templateRef='timing'&gt;](/out/md/cml/adf_log/timing-d3e4389)

![](/imgs/ADF_module_timing.png)

## Input file

Data source: [&lt;module cmlx:templateRef='input.file'&gt;](/out/md/cml/adf_log/input.file-d3e5751)

![](/imgs/ADF_module_inputfile.png)

[^1]: string `adf:getCalcType` string `runtype` boolean `hasVibrations` boolean `isMininum` boolean `isQuild` boolean `isNMR`

    ```xml
                                
        $runtype        Refers to <scalar dataType="xsd:string" dictRef="cc:runtype">
        $hasVibrations  Exists module <module cmlx:templateRef="vibrations" > ?
        $isMinimum      All frequencies from <module cmlx:templateRef="vibrations" > are positive?
        $isQuild        Exists module <module cmlx:templateRef="quild.iteration" > ?
        $isNMR          Exists module <module cmlx:templateRef="nucleus" > ?                            
                   
        
        <!-- Calculation type related constants -->
        <xsl:variable name="adf:GeometryOptimization" select="'Geometry optimization'" />
        <xsl:variable name="adf:SinglePoint" select="'Single point'" />
        <xsl:variable name="adf:TransitionState" select="'TS'" />
        <xsl:variable name="adf:Frequencies" select="'Frequencies'" />
        <xsl:variable name="adf:Minimum" select="'Minimum'"/>
        <xsl:variable name="adf:Quild" select="'Quild'" />    
        <xsl:variable name="adf:NMR" select="'NMR'" />
        
        <!-- Calculation type variables -->
        <xsl:variable name="calcType" select="
            if(compare($runType,'GEOMETRY OPTIMIZATION') = 0) 
                then $adf:GeometryOptimization 
            else
                if(compare($runType,'SINGLE POINT') = 0)
                    then $adf:SinglePoint
                else
                    if(compare($runType,'TRANSITION STATE') = 0)
                        then $adf:TransitionState
                    else
                        if(compare($runType,'FREQUENCIES') = 0)
                            then $adf:Frequencies
                        else
                            $adf:SinglePoint" />              
        
        <xsl:variable name="vibrations" select="
            if($hasVibrations)
                then if($isMinimum)
                        then concat(' ', $adf:Minimum)
                     else
                         if(compare($calcType,$adf:TransitionState) != 0) 
                             then concat(' ',$adf:TransitionState)
                         else 
                             ''
            else ''" />
            
        <xsl:variable name="quild" select="
            if($isQuild)
                then concat(' ',$adf:Quild)
            else
                ''" />
            
        <xsl:variable name="nmr" select="
            if($isNMR)
                then concat(' ',$adf:NMR)
            else
                ''"
        />
        <xsl:sequence select="concat($calcType, $vibrations, $quild, $nmr)"/>                              
                            
                            
    ```