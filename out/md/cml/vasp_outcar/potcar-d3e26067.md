# potcar {#potcar-d3e26067}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | potcar                                                                                                                                              |
| name                                                                                                                                                | Potcar resume section                                                                                                                               |
| pattern                                                                                                                                             | \\s\*POTCAR.\*\$\\s\\s.\*                                                                                                                           |
| endPattern                                                                                                                                          | \\s\*\$\\s\*                                                                                                                                        |
| endPattern2                                                                                                                                         | \\s\*(POSCARIEXHCAR:).\*                                                                                                                            |
| endPattern3                                                                                                                                         | \\s\*-{30}\\s\*                                                                                                                                     |
| endPattern4                                                                                                                                         | \\s\*\\S+\\s+\\w\\w?\\w?\\s+\\S+\\s\*:\\s\*                                                                                                         |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | potcar/potcar.xml                                                                                                                                   |

######Template attributes

**Comment.**

           
     POTCAR:    PAW_PBE Ce 23Dec2003                  
       VRHFIN =Ce : [core= Kr 4d10]                                                 
       LEXCH  = PE                                                                  
       EATOM  =  1063.0861 eV,   78.1346 Ry                                         
                                                                                    
       TITEL  = PAW_PBE Ce 23Dec2003                                                
       LULTRA =        F    use ultrasoft PP ?                                      
       IUNSCR =        1    unscreen: 0-lin 1-nonlin 2-no                           
       RPACOR =    1.800    partial core radius                                     
       POMASS =  140.115; ZVAL   =   12.000    mass and valenz                      
       RCORE  =    2.700    outmost cutoff radius                                   
       RWIGS  =    2.500; RWIGS  =    1.323    wigner-seitz radius (au A)           
       ENMAX  =  273.042; ENMIN  =  204.781 eV                                      
       RCLOC  =    1.810    cutoff for local pot                                    
       LCOR   =        T    correct aug charges                                     
       LPAW   =        T    paw PP                                                  
       EAUG   =  580.196                                                            
       DEXC   =    0.000                                                            
       RMAX   =    2.749    core radius for proj-oper                               
       RAUG   =    1.300    factor for augmentation sphere                          
       RDEP   =    2.810    radius for radial grids                                 
       RDEPT  =    2.162    core radius for aug-charge                              
                                                                                    
       Atomic configuration                                                         
       14 entries                                                                   
         n  l   j            E        occ.                                          
         1  0  0.50    -40258.9816   2.0000                                         
         2  0  0.50     -6445.4884   2.0000                                         
         2  1  1.50     -5771.7470   6.0000                                         
         3  0  0.50     -1387.9739   2.0000                                         
         3  1  1.50     -1173.8158   6.0000                                         
         3  2  2.50      -869.9108  10.0000                                         
         4  0  0.50      -280.8706   2.0000                                         
         4  1  1.50      -210.9815   6.0000                                         
         4  2  2.50      -110.4558  10.0000                                         
         5  0  0.50       -40.5819   2.0000                                         
         6  0  0.50        -3.7444   2.0000                                         
         5  1  1.50       -23.2188   6.0000                                         
         5  2  2.50        -3.0598   1.0000                                         
         4  3  2.50        -5.3970   1.0000                                         
       Description                                                                  
         l       E           TYP  RCUT    TYP  RCUT                                 
         0    -40.5819164     23  1.500                                             
         0     -3.7443793     23  2.300                                             
         1    -23.2188445     23  2.000                                             
         1     40.8174780     23  2.300                                             
         2     -3.0597556     23  2.500                                             
         2     13.6058260     23  2.500                                             
         3     -5.3970469     23  2.700                                             
         3     -5.8505052     23  2.700                                             
      local pseudopotential read in
      partial core-charges read in
      partial kinetic energy density read in
      atomic valenz-charges read in
      non local Contribution for L=           0  read in
        real space projection operators read in
      non local Contribution for L=           0  read in
        real space projection operators read in
      non local Contribution for L=           1  read in
        real space projection operators read in
      non local Contribution for L=           1  read in
        real space projection operators read in
      non local Contribution for L=           2  read in
        real space projection operators read in
      non local Contribution for L=           2  read in
        real space projection operators read in
      non local Contribution for L=           3  read in
        real space projection operators read in
      non local Contribution for L=           3  read in
        real space projection operators read in
        PAW grid and wavefunctions read in
     
       number of l-projection  operators is LMAX  =           8
       number of lm-projection operators is LMMAX =          32
     
     POTCAR:    PAW_PBE H 15Jun2001                   
       VRHFIN =H: ultrasoft test                                                    
       LEXCH  = PE                                                                  
     ...
     
     POSCAR: CIF file 
        

**Comment.**

-   [atom.potcar](/out/md/cml/vasp_outcar/atom.potcar-d3e26074.md)


