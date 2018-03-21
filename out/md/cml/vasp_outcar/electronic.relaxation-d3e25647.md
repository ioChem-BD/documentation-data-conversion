# electronic.relaxation {#electronic.relaxation-d3e25647}

VASP outcar

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | electronic.relaxation                                                                                                                               |
| name                                                                                                                                                | Electronic relaxation                                                                                                                               |
| pattern                                                                                                                                             | \\s\*Electronic\\sRelaxation.\*                                                                                                                     |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| endPattern2                                                                                                                                         | \\s\*Ionic.\*                                                                                                                                       |
| xml:base                                                                                                                                            | electronic.relaxation.xml                                                                                                                           |

######Template attributes

**Input.**

     Electronic Relaxation 1
       ENCUT  =  500.0 eV  36.75 Ry    6.06 a.u.  14.17 14.17 41.81*2*pi/ulx,y,z
       ENINI  =  500.0     initial cutoff
       ENAUG  =  644.9 eV  augmentation charge cutoff
       NELM   =    250;   NELMIN=  2; NELMDL=  0     # of ELM steps 
       EDIFF  = 0.1E-04   stopping-criterion for ELM
       LREAL  =      T    real-space projection
       NLSPLINE    = F    spline interpolate recip. space projectors
       LCOMPAT=      F    compatible to vasp.4.4
       GGA_COMPAT  = T    GGA compatible to vasp.4.4-vasp.4.6
       LMAXPAW     = -100 max onsite density
       LMAXMIX     =    6 max onsite mixed and CHGCAR
       VOSKOWN=      0    Vosko Wilk Nusair interpolation
       ROPT   =   -0.00050  -0.00050  -0.00050  -0.00050    
        
        

**Output text.**

```xml
<comment class="example.output" id="electronic.relaxation">   
        <module cmlx:templateRef="electronic.relaxation">        
            <module>
                <list cmlx:templateRef="missingID">
                    <scalar dataType="xsd:integer" dictRef="v:energyCutoff" units="nonsi:electronvolt">500</scalar>
                </list>
            </module>
            <module>
                <list cmlx:templateRef="missingID">
                    <scalar dataType="xsd:double" dictRef="v:ediff">0.1E-04</scalar>
                </list>
            </module>
        </module>         
    </comment>
```
