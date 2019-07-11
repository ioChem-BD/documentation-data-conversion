# casscf {#casscf-d3e19781}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | casscf                                                                                                                                              |
| name                                                                                                                                                | CASSCF section                                                                                                                                      |
| pattern                                                                                                                                             | \\s\*-{70,}\$\\s\*ORCA-CASSCF\\s\*\$\\s\*-{70,}                                                                                                     |
| endPattern                                                                                                                                          | \\s\*-{70,}\\s\*\$\\s\*\\S+.\*\$\\s\*\\S+.\*                                                                                                        |
| endPattern2                                                                                                                                         | \\s\*\\\*{20,}\\s\*                                                                                                                                 |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | casscf/casscf.xml                                                                                                                                   |

######Template attributes

**Comment.**

    ------------------------------------------------------------------------------
                                  ORCA-CASSCF
    ------------------------------------------------------------------------------

    Setting up the integral package       ... done
    Building the CAS space                ... done (1037 configurations for Mult=3)
    Building the CAS space                ... done (1107 configurations for Mult=1)
    ----------------
    GENERAL CI SETUP
    ----------------
    ...
    ------------------
    CAS-SCF ITERATIONS
    ------------------
    ...
    --------------
    CASSCF RESULTS
    --------------
    ...
    ----------------
    ORBITAL ENERGIES
    ----------------
    ...
    ---------------------------------------------
    CAS-SCF STATES FOR BLOCK  1 MULT= 3 NROOTS= 4
    ---------------------------------------------
    ...
    -----------------------------
    SA-CASSCF TRANSITION ENERGIES
    ------------------------------
    ...
    --------------
    DENSITY MATRIX
    --------------
    ...
    -------------------
    SPIN-DENSITY MATRIX
    -------------------
    ...
    -----------------
    ENERGY COMPONENTS
    -----------------
    ...
    ----------------------------
    LOEWDIN ORBITAL-COMPOSITIONS
    ----------------------------
    ...
    ----------------------------
    LOEWDIN REDUCED ACTIVE MOs  
    ----------------------------
    ...
