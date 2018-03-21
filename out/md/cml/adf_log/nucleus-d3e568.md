# nucleus {#nucleus-d3e568}

ADF log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | nucleus                                                                                                                                             |
| name                                                                                                                                                | NMR nucleus                                                                                                                                         |
| pattern                                                                                                                                             | .\*N\\sU\\sC\\sL\\sE\\sU\\sS\\s:.\*                                                                                                                 |
| endPattern                                                                                                                                          | \\s\*\#{20,}\\s\*                                                                                                                                   |
| endPattern2                                                                                                                                         | \\s?\\\*{20,}\\s\*                                                                                                                                  |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | nucleus.xml                                                                                                                                         |

######Template attributes

**Input.**

    ****  N U C L E U S : W(23)
    ... 
    ================================================================================
     
     
    === SCALED: PARAMAGNETIC NMR SHIELDING TENSORS (ppm)
    ...
                            ***********************************
                            CARTESIAN AXIS REPRESENTATION
    ...
                            isotropic shielding =  -7015.324
     
    ================================================================================
     
     
    === SCALED: DIAMAGNETIC NMR SHIELDING TENSORS (ppm)
    ...
                            ***********************************
                            CARTESIAN AXIS REPRESENTATION
    ...
                            isotropic shielding =   9657.458

    ================================================================================ 
     
    === SCALED: SPIN-ORBIT NMR SHIELDING TENSORS (ppm)
    ...
                            ***********************************
                            CARTESIAN AXIS REPRESENTATION
    ...
                            isotropic shielding =   -162.648 
    ================================================================================
     
     
    === SCALED: TOTAL NMR SHIELDING TENSOR (ppm)
    ... 
                            ***********************************
                            CARTESIAN AXIS REPRESENTATION
    ...
                            isotropic shielding =   2479.486

    ################################################################################
    ********************************************************************************
    ****  N U C L E U S : W(22)
    ...
    === SCALED: PARAMAGNETIC NMR SHIELDING TENSORS (ppm)
    ...
                            ***********************************
                            CARTESIAN AXIS REPRESENTATION
    ...
                            isotropic shielding =  -7001.298
                            
    ================================================================================

    === SCALED: DIAMAGNETIC NMR SHIELDING TENSORS (ppm)
                             ***********************************
                            CARTESIAN AXIS REPRESENTATION
    ...
                            isotropic shielding =   9657.950

    ================================================================================ 
     
    === SCALED: SPIN-ORBIT NMR SHIELDING TENSORS (ppm)
    ...
                             ***********************************
                            CARTESIAN AXIS REPRESENTATION

                            isotropic shielding =   -167.181

    ================================================================================ 
     
    === SCALED: TOTAL NMR SHIELDING TENSOR (ppm)
     
                            ***********************************
                            CARTESIAN AXIS REPRESENTATION
    ...
                            isotropic shielding =   2489.471

    ################################################################################
        

> **Warning**
>
> Current template has input comments defined but it's output is missing, please notify data architects.
