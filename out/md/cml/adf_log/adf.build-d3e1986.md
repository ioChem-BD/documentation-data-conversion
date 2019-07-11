# adf.build {#adf.build-d3e1986}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | adf.build                                                                                                                                           |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| pattern                                                                                                                                             | \\s+\\\*\\s+B\\sU\\sI\\sL\\sD\\s\\:\\s\\(Fragments\\,\\sFunctions\\).\*                                                                             |
| endPattern                                                                                                                                          | \\s\*\\d\*\\s\*\$\\s\\\*{20,}.\*\$(\\s\*I\\s\*LOGFILE.\*)                                                                                           |
| offset                                                                                                                                              | -1                                                                                                                                                  |
| endOffset                                                                                                                                           | 2                                                                                                                                                   |
| xml:base                                                                                                                                            | build/build\_fragments.xml                                                                                                                          |

######Template attributes

**Comment.**

                                          ****************************************
                                          *  B U I L D : (Fragments, Functions)  *
                                          ****************************************
                                         
     =======
     S F O s  ***  (Symmetrized Fragment Orbitals)  ***
     =======
      
     SFOs are linear combinations of (valence) Fragment Orbitals (FOs), such that the SFOs transform as the
     irreducible representations of the (molecular) symmetry group. Each SFO is therefore characterized by
     an irrep of the molecule and by a few (or only one) generating FOs
     
     ....

     ***************************************************************************************************
        
        
