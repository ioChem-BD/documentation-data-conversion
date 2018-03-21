# adf.results {#adf.results-d3e2463}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | adf.results                                                                                                                                         |
| pattern                                                                                                                                             | \\s\*\\\*\\s\*R\\sE\\sS\\sU\\sL\\sT\\sS\\s\*\\\*.\*                                                                                                 |
| endPattern                                                                                                                                          | \\s\*\\W\*\\s\*\$\\s\*\\\*{20,}.\*\$(\\s\*I\\s\*LOGFILE.\*)                                                                                         |
| offset                                                                                                                                              | -1                                                                                                                                                  |
| endOffset                                                                                                                                           | 2                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | results/results.xml                                                                                                                                 |

######Template attributes

**Comment.**

                                                    *******************
                                                    *  R E S U L T S  *
                                                    *******************
     
     
     Orbital Energies, all Irreps
     ========================================

     Irrep        no.  (spin)   Occup              E (au)                E (eV)
     ---------------------------------------------------------------------------
     F             1            14.00       -0.36757674632897E+00       -10.0023
     D             2             0.00        0.59810837659445E-01         1.6275
    ...
                                                    
     Orbital Energies, all Irreps, both Spins
     ========================================

     Irrep        no.  (spin)   Occup              E (au)                E (eV)
     ---------------------------------------------------------------------------
     A1            1     A       1.00       -0.22582773237906E+01       -61.4509
     A1            1      B      1.00       -0.22573719983754E+01       -61.4262
     A1            2     A       1.00       -0.22570204339745E+01       -61.4167
    ...

     =======================================================
     S F O   P O P U L A T I O N S ,   M O   A N A L Y S I S
     =======================================================
     ...

                                                    
     Fit test: (difference of exact and fit density, squared integrated, result summed over spins)
             Sum-of-Fragments:                             0.00000604855883
             Orthogonalized Fragments:                     0.01126932738939
             SCF:                                          0.00379056264226
    ...
     
     =======================================
     M U L L I K E N   P O P U L A T I O N S
     =======================================
    ...

     =========================================
     Quadrupole Moment (Buckingham convention)  ***  (a.u.)  ***
     =========================================
    ...

     ==========
     S**2 value  ***  see also R. Bulo et al., J.Am.Chem.Soc., 124 (2002) 13903-13910, note (29)  ***
     ==========
    ...

     ===========================
     B O N D I N G   E N E R G Y  ***  (decomposition)  ***
     ===========================
    ...

     ***************************************************************************************************    
        

-   [orbital.energies](/out/md/cml/adf_log/orbital.energies-d3e2470)

<!-- -->

-   [orbital.energies.spin](/out/md/cml/adf_log/orbital.energies.spin-d3e2511)

<!-- -->

-   [fit.test](/out/md/cml/adf_log/fit.test-d3e2555)

<!-- -->

-   [mulliken](/out/md/cml/adf_log/mulliken-d3e2608)

<!-- -->

-   [multipole](/out/md/cml/adf_log/multipole-d3e2798)

<!-- -->

-   [quadrupole.moment](/out/md/cml/adf_log/quadrupole.moment-d3e2958)

<!-- -->

-   [s2](/out/md/cml/adf_log/s2-d3e2987)

<!-- -->

-   [bonding.energy](/out/md/cml/adf_log/bonding.energy-d3e3015)

<!-- -->

-   [sfo.population](/out/md/cml/adf_log/sfo.population-d3e3118)

<!-- -->

-   [excitation.energy](/out/md/cml/adf_log/excitation.energy-d3e3539)


