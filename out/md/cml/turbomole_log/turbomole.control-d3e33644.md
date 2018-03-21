# turbomole.control {#turbomole.control-d3e33644}


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
            
        

-   [atoms](/out/md/cml/turbomole_log/atoms-d3e33651.md)

<!-- -->

-   [methods](/out/md/cml/turbomole_log/methods-d3e33811.md)

<!-- -->

-   [vibrations](/out/md/cml/turbomole_log/vibrations-d3e33857.md)

<!-- -->

-   [dispersion](/out/md/cml/turbomole_log/dispersion-d3e33956.md)

<!-- -->

-   [soes](/out/md/cml/turbomole_log/soes-d3e33978.md)

<!-- -->

-   [parameters](/out/md/cml/turbomole_log/parameters-d3e34038.md)

<!-- -->

-   [orbitals.control](/out/md/cml/turbomole_log/orbitals.control-d3e34157.md)


