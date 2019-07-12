# eigenvalues {#eigenvalues-d3e27921}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | eigenvalues                                                                                                                                         |
| name                                                                                                                                                | Eigenvalues section                                                                                                                                 |
| pattern                                                                                                                                             | \\s\*spin\\scomponent.\*                                                                                                                            |
| pattern2                                                                                                                                            | \\s\*k-point.\*\$\\s\*band\\sNo\\.\\s\*band\\senergies.\*                                                                                           |
| endPattern                                                                                                                                          | \\s\*-{30,}\\s\*                                                                                                                                    |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| keep                                                                                                                                                | last                                                                                                                                                |
| xml:base                                                                                                                                            | eigenvalues/eigenvalues.xml                                                                                                                         |

######Template attributes

**Comment.**

     spin component 1

     k-point   1 :       0.0000    0.0000    0.0000
      band No.  band energies     occupation 
          1     -34.0788      1.00000
          2     -33.9756      1.00000
          3     -33.9665      1.00000
          4     -33.9659      1.00000
    ...
    --------------------------------------------------------------------------------------------------------
        
        

**Comment.**

-   [spin](/out/md/cml/vasp_outcar/spin-d3e27928.md)

<!-- -->

-   [nospin](/out/md/cml/vasp_outcar/nospin-d3e27990.md)


