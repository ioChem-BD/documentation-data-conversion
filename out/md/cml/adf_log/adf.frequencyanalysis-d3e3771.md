# adf.frequencyanalysis {#adf.frequencyanalysis-d3e3771}

ADF log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | ADF log                                                                                                                                                                                               |
| id                                                                                                                                                                                                    | adf.frequencyanalysis                                                                                                                                                                                 |
| name                                                                                                                                                                                                  | Frequency analysis                                                                                                                                                                                    |
| pattern                                                                                                                                                                                               | \\s+\\\*\\s+F\\sR\\sE\\sQ\\sU\\sE\\sN\\sC\\sY\\s+A\\sN\\sA\\sL\\sY\\sS\\sI\\sS\\s+\\\*.\*                                                                                                             |
| endPattern                                                                                                                                                                                            | \\s\*\\d\*\\s\*\$\\s\\\*{20,}.\*\$(\\s\*I\\s\*LOGFILE.\*)                                                                                                                                             |
| offset                                                                                                                                                                                                | -1                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 2                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | frequencyanalysis/frequencyanalysis.xml                                                                                                                                                               |

######Template attributes

**Comment.**

                                         ******************************************
                                         *  F R E Q U E N C Y    A N A L Y S I S  *
                                         ******************************************
    ...


     Zero-Point Energy :      0.500175 a.u.
     ===================     13.610451 eV
     (imaginary frequencies were excluded from the summation) 
     ...
     
     ===========================
     Vibrations and Normal Modes  ***  (cartesian coordinates, NOT mass-weighted)  ***
     ===========================
      
     The headers on the normal mode eigenvectors below give the Frequency in cm-1
     (a negative value means an imaginary frequency, no output for (almost-)zero frequencies)


                           -28.256                        45.406                        54.750
                  ------------------------      ------------------------      ------------------------
        1.C         -0.012   0.007  -0.020         0.041  -0.105  -0.038        -0.005  -0.030   0.101
        2.C         -0.004   0.034  -0.019         0.035  -0.097  -0.044         0.022  -0.037   0.100
        3.C         -0.019   0.001  -0.004         0.012  -0.113  -0.038        -0.023  -0.039   0.094
        4.C          0.010   0.043   0.000         0.012  -0.104  -0.038         0.022  -0.031   0.099
        5.C          0.009   0.029   0.012        -0.054  -0.129  -0.034        -0.011  -0.035   0.098
        6.C          0.013  -0.016  -0.022         0.029  -0.099  -0.038        -0.025  -0.028   0.091
        7.C         -0.014   0.051  -0.027         0.008  -0.086  -0.036         0.024  -0.034   0.095
        8.C         -0.026  -0.035  -0.003         0.039  -0.084  -0.047        -0.048  -0.056   0.074
        9.C          0.006   0.066   0.001         0.021  -0.076  -0.020         0.043  -0.007   0.095

    ...
        
     List of All Frequencies:


     Intensities
     ===========

                   Frequency       Dipole Strength        Absorption Intensity (degeneracy not counted)
                     cm-1           1e-40 esu2 cm2          km/mole
                  ----------          ----------          ----------
                  -28.256192           39.676107           -0.281009
                   45.405798           70.141843            0.798301
                   54.750200          154.864558            2.125278
     ...
            
     ============================
     Statistical Thermal Analysis  ***  ideal gas assumed  ***
     ============================
      
     Pressure:                  1.000000 atm.
     Temperature:             300.000000 K



     Moments of Inertia (and direction vectors)
     ==========================================

           41342.8675      42584.1405      47497.7524
     ...
                              
     ***************************************************************************************************
     
        

-   [zeropoint](/out/md/cml/adf_log/zeropoint-d3e3778.md)

<!-- -->

-   [vibrations](/out/md/cml/adf_log/vibrations-d3e3809.md)

<!-- -->

-   [intensities](/out/md/cml/adf_log/intensities-d3e3887.md)

<!-- -->

-   [thermochemistry](/out/md/cml/adf_log/thermochemistry-d3e3926.md)


