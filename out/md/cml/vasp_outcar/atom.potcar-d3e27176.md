# atom.potcar {#atom.potcar-d3e27176}

VASP outcar

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Partial.png)                                                                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | VASP outcar                                                                                                                                                                                           |
| id                                                                                                                                                                                                    | atom.potcar                                                                                                                                                                                           |
| name                                                                                                                                                                                                  | Potcar resume section                                                                                                                                                                                 |
| pattern                                                                                                                                                                                               | \\s\*POTCAR:.\*\$\\s{2,}\\w.\*                                                                                                                                                                        |
| endPattern                                                                                                                                                                                            | \\s\\w.\*                                                                                                                                                                                             |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | atom.potcar.xml                                                                                                                                                                                       |

######Template attributes

**Input.**

     POTCAR:   PAW_GGA O 05Jan2001                    
       VRHFIN =O: s2p4                                                              
       LEXCH  = 91                                                                  
       EATOM  =   433.0277 eV,   31.8266 Ry                                         
                                                                                    
       TITEL  = PAW_GGA O 05Jan2001                                                 
       LULTRA =        F    use ultrasoft PP ?                                      
       IUNSCR =        0    unscreen: 0-lin 1-nonlin 2-no                           
       RPACOR =     .000    partial core radius                                     
       POMASS =   16.000; ZVAL   =    6.000    mass and valenz                      
       RCORE  =    1.520    outmost cutoff radius                                   
       RWIGS  =    1.550; RWIGS  =     .820    wigner-seitz radius (au A)           
       ENMAX  =  400.000; ENMIN  =  300.000 eV                                      
       ICORE  =        2    local potential                                         
       LCOR   =        T    correct aug charges                                     
       LPAW   =        T    paw PP                                                  
       EAUG   =  605.392                                                            
       DEXC   =     .000                                                            
       RMAX   =    2.264    core radius for proj-oper                               
       RAUG   =    1.300    factor for augmentation sphere                          
       RDEP   =    1.550    radius for radial grids                                 
       QCUT   =   -5.520; QGAM   =   11.040    optimization parameters              
                                                                                    
       Description                                                                  
         l     E      TYP  RCUT    TYP  RCUT                                        
         0   .000     23  1.200                                                     
         0  -.700     23  1.200                                                     
         1   .000     23  1.520                                                     
         1   .600     23  1.520                                                     
         2   .000      7  1.500                                                     
      local pseudopotential read in
      atomic valenz-charges read in
      non local Contribution for L=           0  read in
        real space projection operators read in
      non local Contribution for L=           0  read in
        real space projection operators read in
      non local Contribution for L=           1  read in
        real space projection operators read in
      non local Contribution for L=           1  read in
        real space projection operators read in
        PAW grid and wavefunctions read in
     
       number of l-projection  operators is LMAX  =           4
       number of lm-projection operators is LMMAX =           8
     
     PAW_GGA Ti 08Aug2001                   :   
        

**Output text.**

```xml
<comment class="example.output" id="atom.potcar"> 
        <module cmlx:templateRef="atom:potcar">
            <scalar dataType="xsd:string" dictRef="v:pseudopotential">PAW_PBE O 08Apr2002</scalar>
            <scalar dataType="xsd:string" dictRef="cc:atomType">O</scalar>
            <scalar dataType="xsd:double" dictRef="cc:mass">16.000</scalar>
            <scalar dataType="xsd:double" dictRef="cc:valence">6.000</scalar>
        </module> 
    </comment>
```
