# molecular.orbitals {#molecular.orbitals-d3e24562}

Turbomole log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole log                                                                                                                                       |
| id                                                                                                                                                  | molecular.orbitals                                                                                                                                  |
| name                                                                                                                                                | Molecular orbitals                                                                                                                                  |
| pattern                                                                                                                                             | \\s\*orbitals.\*will\\sbe\\swritten\\sto\\sfile.\*                                                                                                  |
| endPattern                                                                                                                                          | \\s\*IRREP.\*I\\s\*\\----|.\*I\\s\*\\WS\\\*S\\W.\*                                                                                                     |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| xml:base                                                                                                                                            | molecularorbitals/molecular.orbitals.xml                                                                                                            |

######Template attributes

**Comment.**

         orbitals $scfmo  will be written to file mos

        irrep                  1a1'        2a1'        3a1'        4a1'        5a1'
     eigenvalues H       -256.02776   -29.97174   -10.18645    -3.38954    -0.88456
                eV       -6966.9251   -815.5790   -277.1896    -92.2348    -24.0702
     occupation              2.0000      2.0000      2.0000      2.0000      2.0000

        irrep                  6a1'        7a1'        8a1'        9a1'       10a1'
     eigenvalues H         -0.52760    -0.40581    -0.22513     0.04248     0.15326
                eV         -14.3569    -11.0428     -6.1262      1.1561      4.1703
    ...
        

**Comment.**

         orbitals $uhfmo_beta  will be written to file beta

     orbitals $uhfmo_alpha  will be written to file alpha

     alpha:

        irrep                 70ag        71ag        72ag        73ag        74ag
     eigenvalues H         -0.51661    -0.51394    -0.50049    -0.46949    -0.45831
                eV         -14.0577    -13.9851    -13.6190    -12.7756    -12.4715
     occupation              1.0000      1.0000      1.0000      1.0000      1.0000

    ...

     beta:

        irrep                 66ag        67ag        68ag        69ag        70ag
     eigenvalues H         -0.52481    -0.51885    -0.51455    -0.51425    -0.41476
                eV         -14.2810    -14.1187    -14.0018    -13.9937    -11.2862
     occupation              1.0000      1.0000      1.0000      1.0000      1.0000

     ...
        
        

-   [restricted.orbitals](/out/md/cml/turbomole_log/restricted.orbitals-d3e24572.md)

<!-- -->

-   [unrestricted.orbitals](/out/md/cml/turbomole_log/unrestricted.orbitals-d3e24691.md)


