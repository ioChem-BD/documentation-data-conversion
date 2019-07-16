# input.file {#input.file-d3e35135}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Partial.png)                                                                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | MOPAC log                                                                                                                                                                                             |
| id                                                                                                                                                                                                    | input.file                                                                                                                                                                                            |
| name                                                                                                                                                                                                  | Input file section                                                                                                                                                                                    |
| pattern                                                                                                                                                                                               | \\s\*\\\*+\\s\*\$\\s\*\\\*\\s\*CALCULATION\\sDONE:.\*                                                                                                                                                 |
| endPattern                                                                                                                                                                                            | \\s\*\$\\s\*\$\\s\*                                                                                                                                                                                   |
| startOffset                                                                                                                                                                                           | 2                                                                                                                                                                                                     |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | input.xml                                                                                                                                                                                             |

######Template attributes

**Input.**

     *******************************************************************************
     *  CALCULATION DONE:                                Fri Jan  6 19:51:47 2017  *
     *  PM6        - The PM6 Hamiltonian to be used
     *  MOZYME     - USE LOCALIZED M.O.s IN SOLVING THE SCF EQUATIONS
     *  PRECISE    - CRITERIA TO BE INCREASED BY 100 TIMES
     *  T=         - A TIME OF 172800.0 SECONDS REQUESTED
     *  DUMP=N     - RESTART FILE WRITTEN EVERY  7200.000 SECONDS
     *  AUX        - OUTPUT AUXILIARY INFORMATION
     *  PRTXYZ     - PRINT CARTESIAN COORDINATES
     *  PRNT       - EXTRA PRINTING IN EF ROUTINE
     *  DISP       - PRINT DISPERSION AND HYDROGEN BOND ENERGIES
     *  PL         - MONITOR CONVERGENCE IN DENSITY MATRIX
     *******************************************************************************
    PM6 MOZYME PRECISE PRTXYZ PRNT=5 DISP(1.0) PL AUX
      AI
     PM6 optimization
       ATOM   CHEMICAL          X               Y               Z
      NUMBER   SYMBOL      (ANGSTROMS)     (ANGSTROMS)     (ANGSTROMS)
     
         1       C         -4.19184475  *   2.56171882  *   1.35180722  *
         2       C         -4.85437358  *   3.57297417  *   0.50049748  *
         3       C         -6.22952321  *   3.62747474  *   0.39522324  *
         4       C         -7.13930258  *   2.80943244  *   1.25599220  *
         5       C         -6.41595323  *   1.70580884  *   2.18557431  *
         6       C         -4.92595752  *   1.63926235  *   2.06986776  *
      
           
        

**Output text.**

```xml
<comment class="example.output" id="input.file">
       <module cmlx:templateRef="input.file">    
          <module cmlx:templateRef="inputlines">
             <list cmlx:templateRef="lines">
                <scalar dataType="xsd:string" dictRef="mp:inputline">*******************************************************************************</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  CALCULATION DONE:                                Fri Jan  6 19:51:47 2017  *</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  PM6        - The PM6 Hamiltonian to be used</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  MOZYME     - USE LOCALIZED M.O.s IN SOLVING THE SCF EQUATIONS</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  PRECISE    - CRITERIA TO BE INCREASED BY 100 TIMES</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  T=         - A TIME OF 172800.0 SECONDS REQUESTED</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  DUMP=N     - RESTART FILE WRITTEN EVERY  7200.000 SECONDS</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  AUX        - OUTPUT AUXILIARY INFORMATION</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  PRTXYZ     - PRINT CARTESIAN COORDINATES</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  PRNT       - EXTRA PRINTING IN EF ROUTINE</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  DISP       - PRINT DISPERSION AND HYDROGEN BOND ENERGIES</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*  PL         - MONITOR CONVERGENCE IN DENSITY MATRIX</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">*******************************************************************************</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">PM6 MOZYME PRECISE PRTXYZ PRNT=5 DISP(1.0) PL AUX</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">AI</scalar>
                <scalar dataType="xsd:string" dictRef="mp:inputline">PM6 optimization</scalar>
             </list>
          </module>
          <module cmlx:templateRef="geometry">
            <molecule id="initial">
               <atomArray>
                  <atom elementType="C" id="a1" x3="0.19184475" y3="2.56171882" z3="1.35180722">
                     <scalar dataType="xsd:integer" dictRef="cc:serial">1</scalar>
                     <scalar dataType="xsd:integer" dictRef="g:atomicType">-4</scalar>
                     <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                  </atom>
                  <atom elementType="C" id="a2" x3="0.85437358" y3="3.57297417" z3="0.50049748">
                     <scalar dataType="xsd:integer" dictRef="cc:serial">2</scalar>
                     <scalar dataType="xsd:integer" dictRef="g:atomicType">-4</scalar>
                     <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                  </atom>
                  <atom elementType="C" id="a3" x3="0.22952321" y3="3.62747474" z3="0.39522324">
                     <scalar dataType="xsd:integer" dictRef="cc:serial">3</scalar>
                     <scalar dataType="xsd:integer" dictRef="g:atomicType">-6</scalar>
                     <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                  </atom>
                  <atom elementType="C" id="a4" x3="0.13930258" y3="2.80943244" z3="1.2559922">
                     <scalar dataType="xsd:integer" dictRef="cc:serial">4</scalar>
                     <scalar dataType="xsd:integer" dictRef="g:atomicType">-7</scalar>
                     <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                  </atom>
                  <atom elementType="C" id="a5" x3="0.41595323" y3="1.70580884" z3="2.18557431">
                     <scalar dataType="xsd:integer" dictRef="cc:serial">5</scalar>
                     <scalar dataType="xsd:integer" dictRef="g:atomicType">-6</scalar>
                     <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                  </atom>
                  <atom elementType="C" id="a6" x3="0.92595752" y3="1.63926235" z3="2.06986776">
                     <scalar dataType="xsd:integer" dictRef="cc:serial">6</scalar>
                     <scalar dataType="xsd:integer" dictRef="g:atomicType">-4</scalar>
                     <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                  </atom>
               </atomArray>
          </molecule>
        </module>
       </module>      
    </comment>
```