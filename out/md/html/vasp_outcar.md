# Page components detail

# Header

| Field                                                                                   | Source                                                                                 | Sample value                                                                                                          |
|----|----|----|
| Title                                                                                   | *Set on Browse calculation publication*                                                | Sample calculation                                                                                                    |
| Browse Item                                                                             | *URL pointing Browse published item*                                                   | https://argo.urv.es:8080/jspui/handle/123456789/6                                                                     |
| Program                                                                                 | [&lt;scalar dictRef="cc:program"&gt;](/out/md/cml/vasp_outcar/generator-d3e25529.md) template                    | VASP 5.3.2                                                                                                            |
| Author                                                                                  | *Username fullname*                                                                    | Alvarez Moreno, Moises                                                                                                |
| Formula                                                                                 | *Atom count from final geometry*                                                       | C 1 H 4 Mo 30 O 61                                                                                                    |
| Calculation type                                                                        | Custom logic                                                                           | Geometry optimization                                                                                                 |
| Functional                                                                              | Custom logic                                                                           | PBE+U                                                                                                                 |
| Shell type (ISPIN)                                                                      | [&lt;scalar dictRef="v:ispin"&gt;](/out/md/cml/vasp_outcar/incar-d3e25580.md)                                    | Open Shell                                                                                                            |
| Temperature                                                                             | [&lt;scalar dictRef="cc:temp"&gt;](/out/md/cml/vasp_outcar/incar-d3e25580.md)                                    | 0.0K                                                                                                                  |

######VASP - General Info - Main fields

![](/imgs/VASP_header.png)

[^1]

[^2]

# Settings

Most relevant calculation input parameters. Almost all information fields come from [&lt;module cmlx:templateRef="incar"&gt;](/out/md/cml/vasp_outcar/incar-d3e25580.md)

-   SIGMA

-   ISMEAR

-   LDIPOL

-   IDIPOL

-   Multiplicity

-   NELECT

-   Cut-Off Energy

-   EDIFF

-   EDDIFG

-   POTIM

-   LDAU (LDAUL, LDAUU, LDAUJ)

-   VDW and VDW Version

-   Parameters for Grimme's potential [&lt;module cmlx:templateRef="grimmes"&gt;](/out/md/cml/vasp_outcar/grimmes-d3e26993.md)

![](/imgs/VASP_settings.png)

# Atoms info

After settings section, our HTML resume will output cell coordinates, lattice vectors and a coordinates table with molecule atoms.

Initial geometry its readed from OUTCAR file using :[&lt;module cmlx:templateRef="position"&gt;](#position-d3e26244), [&lt;module cmlx:templateRef="incar"&gt;](/out/md/cml/vasp_outcar/incar-d3e25580.md), [&lt;module cmlx:templateRef="potcar"&gt;](/out/md/cml/vasp_outcar/potcar-d3e26067.md) and [&lt;module
cmlx:templateRef="laticce"&gt;](#lattice-d3e26154)

Final geometry will be generated using the same modules than Initial geometry, but coordinates will come from last instance of [&lt;module cmlx:templateRef="calculated.position"&gt;](/out/md/cml/vasp_outcar/calculated.position-d3e26381.md)

For every atom, we will output it's serial number, atom type, cartesian and fractional coordinates (in angstroms) , and [basis used](/out/md/cml/vasp_outcar/atom.potcar-d3e26074.md).

![](/imgs/VASP_geometry.png)

# Molecular Info

This section captures molecule additional information not captured on previous section.

K-point generation parameters readed form [KPOINTS file](/out/md/cml/vasp_outcar/vasp.kpoints-d3e37348.md)

![](/imgs/VASP_molecularinfo.png)

# Modules

## Energies

Data source: [&lt;module cmlx:templateRef='energy'&gt;](/out/md/cml/vasp_outcar/energy-d3e26584.md)

This module will hold Free ,E0 , dE and E-fermi energies.

In case of single calculations (single point, geometry optimization), a table with this values will be displayed.

On multiple OUTCAR calculations like Nudge Elastic Band (NEB) or Dimmer, a graphic will be printed with each diferential energy as step.

![](/imgs/VASP_module_energies_single.png)

![](/imgs/VASP_module_energies_multiple.png)

## Eigenvalues

Data source: [&lt;module cmlx:templateRef='eigenvalues'&gt;](/out/md/cml/vasp_outcar/eigenvalues-d3e26819.md)

This module will display eigenvalues per spin and kpoint.

![](/imgs/VASP_module_eigenvalues.png)

## DOS

Data source: DOSCAR file [&lt;module cmlx:templateRef='vasp.doscar'&gt;](/out/md/cml/vasp_outcar/vasp.doscar-d3e37390.md)

On calculations where VASP DOSCAR file has been uploaded, a form will be displayed to configure a graph with the Density Of States (DOS) information

In this form we will can select atoms by index, range or atom type, select spin and molecular orbitals. Once all parameters have been set we will add this line to current graph. We can define/delete as much DOS lines as we need.

![](/imgs/VASP_module_dos.png)

## Magnetization

Data source: [&lt;module cmlx:templateRef='magnetization'&gt;](/out/md/cml/vasp_outcar/magnetization-d3e26682.md)

![](/imgs/VASP_module_magnetization.png)

## Vibrations

Data source: [&lt;module cmlx:templateRef='vibrations'&gt;](/out/md/cml/vasp_outcar/vibrations-d3e26519.md)

![](/imgs/VASP_module_vibration.png)

## Structure

Lattice replication

![](/imgs/VASP_module_structure.png)

[^1]: string `vasp:getCalcType` nodeset `ibrion`

    ```xml
        ibrion                   Value of ibrion parameter on <module cmlx:templateRef="convergence.info" >.       
                   
            <xsl:param name="ibrion"/>
                <xsl:choose>
                    <xsl:when test="count($ibrion) > 1 and exists($ibrion[text() = '44'])"><xsl:value-of select="$vasp:ImprovedDimerMethod"/></xsl:when>
                    <xsl:when test="count($ibrion) > 1"><xsl:value-of select="$vasp:NudgedElasticBand"/></xsl:when>
                    <xsl:otherwise>
                        <xsl:choose>
                            <xsl:when test="$ibrion = -1"><xsl:value-of select="$vasp:SinglePoint"/></xsl:when>
                            <xsl:when test="$ibrion = 0"><xsl:value-of select="$vasp:MolecularDynamics"/></xsl:when>
                            <xsl:when test="$ibrion &gt; 0 and $ibrion &lt; 4"><xsl:value-of select="$vasp:GeometryOptimization"/></xsl:when>
                            <xsl:when test="$ibrion &gt; 4 and $ibrion &lt; 9"><xsl:value-of select="$vasp:FrequencyCalculus"/></xsl:when>
                            <xsl:when test="$ibrion = 44"><xsl:value-of select="$vasp:ImprovedDimerMethod"/></xsl:when>
                            <xsl:otherwise><xsl:value-of select="$vasp:NotAvailable"/></xsl:otherwise>
                        </xsl:choose>                                
                    </xsl:otherwise>
                </xsl:choose>
         
                            
    ```

[^2]: string `turbo:getMehod` string `gga` boolean `lhfcalc` number `hfscreen` number `aggac` boolean `luseVdw` number `zabVdw` number `param1`&gt; number `param2` boolean `ldau`

    ```xml
     
            gga, lhfcalc, hfscreen , ...           parameters readed from OUTCAR file <module cmlx:templateRef="incar">                                      
                                
         <xsl:param name="gga"/>
         <xsl:param name="lhfcalc"/>
           
         <xsl:param name="aggac"/>         
         <xsl:param name="hfscreen"/>        
         <xsl:param name="luseVdw"/>
         <xsl:param name="zabVdw"/>
         <xsl:param name="param1"/>
         <xsl:param name="param2"/>        
         <xsl:param name="ldau"/>
         <xsl:choose>
                 <xsl:when test="compare($lhfcalc,'true')=0">
                        <xsl:choose>
                            <xsl:when test="$hfscreen=0.2">HSE06</xsl:when>
                            <xsl:otherwise>HSE03</xsl:otherwise>                        
                        </xsl:choose>
                 </xsl:when>
                 <xsl:when test="compare($luseVdw , 'true')=0 and $aggac = 0.0">
                     <xsl:choose>
                         <xsl:when test="compare($gga,'RE')=0">vdW-DF</xsl:when>
                         <xsl:when test="compare($gga,'OR')=0">optPBE-vdW</xsl:when>
                         <xsl:when test="compare($gga,'BO')=0 and round($param1 * 1000) div 1000 = 0.183 and round($param2 * 100) div 100 = 0.22">optB88-vdW</xsl:when>
                         <xsl:when test="compare($gga,'MK')=0 and round($param1 * 10000) div 10000 = 0.1234 and $param2 = 1.0">optB86d-vdW</xsl:when>
                         <xsl:when test="compare($gga,'ML')=0 and $zabVdw = -1.8867">vdW-DF2</xsl:when>
                         <xsl:otherwise>N/A</xsl:otherwise>
                     </xsl:choose>
                 </xsl:when> 
                 <xsl:when test="compare($gga,'91')=0">PW91</xsl:when>
                 <xsl:when test="compare($gga,'PE')=0">PBE</xsl:when>
                 <xsl:when test="compare($gga,'RP')=0">rPBE</xsl:when>
                 <xsl:when test="compare($gga,'AM')=0">AM05</xsl:when>
                 <xsl:when test="compare($gga,'PS')=0">PBEsol</xsl:when>                          
                 <xsl:otherwise>N/A</xsl:otherwise>             
             </xsl:choose>
             <xsl:if test="compare($ldau,'true')=0">
                 <xsl:text>+U</xsl:text>
             </xsl:if>         
                                
                            
    ```
