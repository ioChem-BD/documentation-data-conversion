# turbomole.control {#turbomole.control-d3e36083}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole control file                                                                                                                              |
| id                                                                                                                                                  | turbomole.control                                                                                                                                   |
| name                                                                                                                                                | Turbomole control file                                                                                                                              |
| xml:base                                                                                                                                            | topTemplate.xml                                                                                                                                     |

######Template attributes

**Comment.**

           
    $symmetry c1
    $atoms
    fe 1                                                                           \
       basis =fe def2-SV(P)
    n  2-7                                                                         \
       basis =n def2-SV(P)
    h  8-31                                                                        \
       basis =h def2-SV(P)
    c  32-61                                                                       \
       basis =c def2-SV(P)
    $soes
    a  4
    #
    # NumForce insertion:
    #
    $scfconv 8
    $drvopt
       frequency analysis only nofreeze
    $hessian  file=hessian
    $dipgrad  file=dipgrad
    $grad  file=gradient
    #
    # end of NumForce insertion.
    #
    $title
    Fe(bipy)3 MLCT
    $operating system unix
        ...
            
        

-   [atoms](/out/md/cml/turbomole_log/atoms-d3e36090.md)

<!-- -->

-   [methods](/out/md/cml/turbomole_log/methods-d3e36250.md)

<!-- -->

-   [vibrations](/out/md/cml/turbomole_log/vibrations-d3e36296.md)

<!-- -->

-   [dispersion](/out/md/cml/turbomole_log/dispersion-d3e36395.md)

<!-- -->

-   [soes](/out/md/cml/turbomole_log/soes-d3e36417.md)

<!-- -->

-   [parameters](/out/md/cml/turbomole_log/parameters-d3e36477.md)

<!-- -->

-   [orbitals.control](/out/md/cml/turbomole_log/orbitals.control-d3e36596.md)


