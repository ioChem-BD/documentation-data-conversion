# vibrations {#vibrations-d3e33996}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole control file                                                                                                                              |
| id                                                                                                                                                  | vibrations                                                                                                                                          |
| pattern                                                                                                                                             | \\s\*\\u0024.\*vibr.\*                                                                                                                              |
| endPattern                                                                                                                                          | \\s\*\\u0024((?!vibr).)\*                                                                                                                           |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | vibrations/vibrations.xml                                                                                                                           |

######Template attributes

**Comment.**

        $vibrational normal modes
      1 1   0.0620255999   0.0275995122  -0.0021577554  -0.0045023090  -0.0987973762
      1 2  -0.0041450350  -0.0423379158  -0.0176741626   0.0223413579  -0.0088204790
      1 3   0.0026579412  -0.0028291549   0.0268291327   0.0026526017   0.0014327176
      1 4   0.0027270842  -0.0072686360  -0.0002323333   0.0015336638   0.0566300676
      1 5   0.0334628967   0.0023545302   0.0032185684  -0.0274030238   0.0012100178
      ...
      
      $vibrational spectrum
    #  mode     symmetry     wave number   IR intensity    selection rules
    #                        cm**(-1)        km/mol         IR     RAMAN
         1                        0.00         0.00000        -       -
         2                        0.00         0.00000        -       -
         3                        0.00         0.00000        -       -
         4                        0.00         0.00000        -       -
         5                        0.00         0.00000        -       -
         6                        0.00         0.00000        -       -
         7        a              36.62         0.50306       YES     YES
         8        a              40.17         0.08176       YES     YES
         9        a              41.40         0.13467       YES     YES
        10        a              43.34         2.45364       YES     YES
        11        a              48.07         0.70156       YES     YES
        12        a              64.06         0.75864       YES     YES
      ...   
        

-   [normal](/out/md/cml/turbomole_log/normal-d3e34003.md)

<!-- -->

-   [spectrum](/out/md/cml/turbomole_log/spectrum-d3e34051.md)

