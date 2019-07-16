# nmr {#nmr-d3e19}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | ADF log                                                                                                                                                                                               |
| id                                                                                                                                                                                                    | nmr                                                                                                                                                                                                   |
| name                                                                                                                                                                                                  | NMR module                                                                                                                                                                                            |
| pattern                                                                                                                                                                                               | \\s+\\\*\\s+\\I\\s+N\\sM\\sR\\s+\\I\\s+\\\*.\*                                                                                                                                                        |
| endPattern                                                                                                                                                                                            | \\s\*N\\s+M\\s+R\\s+E\\s+X\\s+I\\s+T\\s\*                                                                                                                                                             |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| offset                                                                                                                                                                                                | -10                                                                                                                                                                                                   |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | nmr/nmr.xml                                                                                                                                                                                           |

######Template attributes

**Comment.**


     *******************************************************************************
     *                                                                             *
     *  -------------------------------------                                      *
     *   Amsterdam Density Functional  (ADF)         2009.01   September 29th, 2009*
     *  -------------------------------------                                      *
     *                                               Build 200912192153            *
     *                                                                             *
     *                                                                             *
     *                              =================                              *
     *                              I               I                              *
     *                              I     N M R     I                              *
     *                              I               I                              *
     *                              =================                              *
     *                                                                             *
     *                                                                             *
     *   Online information and documentation:  http://www.scm.com                 *
     *   E-mail:  support@scm.com   info@scm.com                                   *
     *                                                                             *
     *   Scientific publications using ADF results must be properly referenced     *
     *   See the User Manuals (or the web site) for recommended citations          *
     *   The terms and conditions of the End User License Agreement apply to       *
     *   the use of ADF, http://www.scm.com/Sales/LicAgreement.html                *
     *                                                                             *
     *************************  pentium64_linux / hpmpi  ***************************
     
     NMR 2009.01  RunTime: Sep20-2011 16:34:49
     
    ...
                   NUCLEAR COORDINATES (ANGSTROMS):
                     --------------------------------

                     C  (  1):       4.7284      2.1304      0.0000
                     O  (  2):       3.3981      2.6699      0.0000
                     O  (  3):       1.6678     -2.3615      2.9062
    ...


     *******************************************************************************

                                 N M R   E X I T

-   [program.header](/out/md/cml/adf_log/program.header-d3e26.md)

<!-- -->

-   [nuclear.coordinates](/out/md/cml/adf_log/nuclear.coordinates-d3e145.md)

<!-- -->

-   [nucleus](/out/md/cml/adf_log/nucleus-d3e568.md)


