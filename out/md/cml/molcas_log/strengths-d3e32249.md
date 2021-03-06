# strengths {#strengths-d3e32249}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | MOLCAS log                                                                                                                                                                                            |
| id                                                                                                                                                                                                    | strengths                                                                                                                                                                                             |
| pattern                                                                                                                                                                                               | \\s\*(\\+\\+)?\\sDipole\\stransition\\sstrengths:\\s\*                                                                                                                                                |
| endPattern                                                                                                                                                                                            | .\*\[0-9\]\\s\*\$\\s\*\\-{10,}\\s\*                                                                                                                                                                   |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | dipole.transition.xml                                                                                                                                                                                 |

######Template attributes

**Input.**

    ++ Dipole transition strengths:
       ----------------------------
        for osc. strength at least   0.10000000E-07
     
             To  From     Osc. strength   Einstein coefficients Ax, Ay, Az (sec-1)  
          Total A (sec-1)  
             -----------------------------------------------------------------------
     --------------------
             1    2       0.44908649       325.42995      0.80491315E+09   904.63533      0.80491438E+09
             1    3       0.84575810       35416547.       371.67035      0.21877027E+10  0.22231196E+10
             1    4       0.25628259E-07  0.88069050      0.84981547       67.607607       69.338113    
             2    3       0.18378757E-02  0.11066907E-06   146669.54       3.5999583       146673.14    
             2    4       0.74450773E-05   691.28023      0.36464401E-01   6.1233748       697.44007    
             2    5       0.14629998E-05   272.48692      0.57067986E-02   2.3234797       274.81610    
             4    5       0.18162739E-01   4637.2607      0.21982961E-01   289886.55       294523.84    
             -----------------------------------------------------------------------
     --------------------   
        

**Input.**

> **Warning**
>
> Current template has input comments defined but it's output is missing, please notify software developers.
