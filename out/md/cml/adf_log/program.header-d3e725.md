# program.header {#program.header-d3e725}

ADF log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | program.header                                                                                                                                      |
| name                                                                                                                                                | Generic program header                                                                                                                              |
| pattern                                                                                                                                             | \\s\*\\\*\\s+Amsterdam\\sDensity\\sFunctional.\*                                                                                                    |
| offset                                                                                                                                              | -3                                                                                                                                                  |
| endPattern                                                                                                                                          | .\*RunTime.\*                                                                                                                                       |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | ../program.header.xml                                                                                                                               |

######Template attributes

**Input.**

     *******************************************************************************
     *                                                                             *
     *  -------------------------------------                                      *
     *   Amsterdam Density Functional  (ADF)         2007.01   August 20, 2007     *
     *  -------------------------------------                                      *
     *                                               Build 200708201257            *
     *                                                                             *
     *                                                                             *
     *                            =====================                            *
     *                            I                   I                            *
     *                            I     X X X X X     I                            *
     *                            I                   I                            *
     *                            =====================                            *
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
     ****************************  pentium_linux_ifc  ******************************
     
     DIRAC 2007.01  RunTime: Oct16-2008 12:08:11    
            

**Input.**

     *******************************************************************************
     *                                                                             *
     *  -------------------------------------                                      *
     *   Amsterdam Density Functional  (ADF)         2014                          *
     *  -------------------------------------                                      *
     *                                               r48167 2015-10-14             *
     *                                                                             *
     *                                                                             *
     *                            =====================                            *
     *                            I                   I                            *
     *                            I     D I R A C     I                            *
     *                            I                   I                            *
     *                            =====================                            *
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
     ********************  x86_64_linux_intel / platform_mpi  **********************
     
     Licensed to: XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
     SCM User ID: XXXXX
      
     DIRAC 2014  RunTime: Mar01-2016 19:27:34  Nodes: 1  Procs: 1        
            

**Output text.**

```xml
<comment class="example.output" id="program.header">
        <module cmlx:templateRef="program.header">
            <scalar dataType="xsd:string" dictRef="cc:program">ADF</scalar>
            <scalar dataType="xsd:integer" dictRef="cc:programVersion">2007</scalar>
            <scalar dataType="xsd:string" dictRef="cc:programSubversion">01</scalar>
            <scalar dataType="xsd:string" dictRef="cc:programDate">August 20, 2007</scalar>
            <scalar dataType="xsd:string" dictRef="cc:compileDate">200708201257</scalar>
            <scalar dataType="xsd:string" dictRef="cc:programFlavour">pentium_linux_ifc</scalar>
            <scalar dataType="xsd:string" dictRef="cc:runDate">Oct16-2008 12:08:11</scalar>
       </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="program.header2">
        <module cmlx:templateRef="program.header">
            <scalar dataType="xsd:string" dictRef="cc:program">ADF</scalar>
            <scalar dataType="xsd:integer" dictRef="cc:programVersion">2014</scalar>
            <scalar dataType="xsd:string" dictRef="a:compilation">r48167</scalar>
            <scalar dataType="xsd:string" dictRef="cc:compileDate">2015-10-14</scalar>
            <scalar dataType="xsd:string" dictRef="cc:programFlavour">x86_64_linux_intel / platform_mpi</scalar>
            <scalar dataType="xsd:string" dictRef="cc:runDate">Mar01-2016 19:27:34  Nodes: 1  Procs: 1</scalar>
         </module>
    </comment>
```
