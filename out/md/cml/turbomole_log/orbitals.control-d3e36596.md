# orbitals.control {#orbitals.control-d3e36596}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole control file                                                                                                                                                                                |
| id                                                                                                                                                                                                    | orbitals.control                                                                                                                                                                                      |
| name                                                                                                                                                                                                  | Orbital section                                                                                                                                                                                       |
| pattern                                                                                                                                                                                               | \\s\*\\u0024(?i:(closedIalphaIbeta))\\sshell.\*                                                                                                                                                       |
| endPattern                                                                                                                                                                                            | \\s\*\\u0024.\*                                                                                                                                                                                       |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | orbitals.xml                                                                                                                                                                                          |

######Template attributes

**Comment.**

    $closed shells
     a       1-39                                   ( 2 )
        

**Comment.**

    $alpha shells
     ag      1-16                                   ( 1 )
     b1g     1-3                                    ( 1 )
     b2g     1-11                                   ( 1 )
     b3g     1-4                                    ( 1 )
     au      1-3                                    ( 1 )
     b1u     1-15                                   ( 1 )
     b2u     1-4                                    ( 1 )
     b3u     1-11                                   ( 1 )
    $beta shells
     ag      1-16                                   ( 1 )
     b1g     1-2                                    ( 1 )
     b2g     1-11                                   ( 1 )
     b3g     1-4                                    ( 1 )
     au      1-2                                    ( 1 )
     b1u     1-15                                   ( 1 )
     b2u     1-4                                    ( 1 )
     b3u     1-11                                   ( 1 )   
        

-   [restrictedorbitals](/out/md/cml/turbomole_log/restrictedorbitals-d3e36606.md)

<!-- -->

-   [unrestrictedorbitals](/out/md/cml/turbomole_log/unrestrictedorbitals-d3e36634.md)


