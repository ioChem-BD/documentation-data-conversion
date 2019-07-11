# input {#input-d3e17572}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | input                                                                                                                                               |
| name                                                                                                                                                | Input file section                                                                                                                                  |
| pattern                                                                                                                                             | \\s\*----|\\s\*\$\\s+INPUT\\sFILE\\s\*\$\\s\*----|\\s\*                                                                                                   |
| endPattern                                                                                                                                          | .\*\\\*\\\*\\\*\\\*END\\sOF\\sINPUT\\\*\\\*\\\*\\\*\\s\*\$\\s\*----|\\s\*                                                                              |
| endOffset                                                                                                                                           | 2                                                                                                                                                   |
| xml:base                                                                                                                                            | input.xml                                                                                                                                           |

######Template attributes

**Comment.**

    ================================================================================
                                           INPUT FILE
    ================================================================================
    NAME = run.inp
    I  1> %PAL NPROCS 1 END
    I  2> ! HF def2-SVP TightSCF Opt
    I  3>
    I  4> %geom Constraints
    I  5>         { A 1 0 2 90.0 C}
    I  6>       end
    I  7>  end
    I  8>
    I  9> %basis basis SV
    I 10>   newGTO O "6-31G" end
    I 11> end
    I 12>
    I 13> * xyzfile 0 1 h2o.xyz
    I 14>
    I 15>
    I 16>
    I 17>
    I 18>                          ****END OF INPUT****
    ================================================================================    
        

**Input.**

    ================================================================================
                                           INPUT FILE
    ================================================================================
    NAME = ch2.inp
    I  1> ! TZVPP TightSCF mrddci3
    I  2> * xyz 0 3
    I  3> C 0 0 0
    I  4> H 0.7 0.5 0
    I  5> H -0.7 0.5 0
    I  6> *
    I  7> 
    I  8> %CASSCF nel 2
    I  9>         norb 2
    I 10>         nevpt2 true
    I 11>         end
    I 12> 
    I 13> $new_job
    I 14> ! TZVPP TightSCF mrddci3
    I 15> * xyz 0 1
    I 16> C 0 0 0
    I 17> H 0.7 0.5 0
    I 18> H -0.7 0.5 0
    I 19> *
    I 20> 
    I 21> %CASSCF nel 2
    I 22>         norb 2
    I 23>         nevpt2 true
    I 24>         end
    I 25> 
    I 26> 
    I 27> 
    I 28> 
    I 29>                          ****END OF INPUT****
    ================================================================================
        

**Input.**

    ================================================================================
                                           INPUT FILE
    ================================================================================
    NAME = phen3.inp
    I  1> ! OPBE opt def2-SV(P) def2-SVP/C TightSCF UNO
    I  2> 
    I  3> %output
    I  4> Print[ P_UNO_OccNum ] = 1
    I  5> end
    I  6> 
    I  7> * xyz 2 5
    I  8>   Fe    -0.000094   -0.001538    0.015314  newgto "def2-TZVP" end
    I  9>   N     -1.301044    0.998903    1.550485  newgto "def2-TZVP" end
    I 10>   N      1.302490   -1.000716    1.549739  newgto "def2-TZVP" end
    I 11>   N      0.877835   -1.039833   -1.732390  newgto "def2-TZVP" end
    I 12>   N      1.803903    1.327699    0.218253  newgto "def2-TZVP" end
    I 13>   N     -1.805188   -1.328750    0.218929  newgto "def2-TZVP" end
    I 14>   N     -0.878918    1.035806   -1.731790  newgto "def2-TZVP" end
    I 15>   C      2.460016   -0.340681    1.821585
    I 16>   C      2.730294    0.885483    1.110808
    I 17>   C     -2.731299   -0.885256    1.111155  newgto "def2-TZVP" end
    I 18>   C     -2.459525    0.340464    1.822082
    I 19>   C      0.463935   -0.550934   -2.934373
    I 20>   C     -0.463690    0.548788   -2.934056
    I 21>   C      2.047074    2.465059   -0.433956
    I 22>   C      3.211011    3.231578   -0.247375
    I 23>   C      4.164130    2.791912    0.656265
    I 24>   C      3.941678    1.589394    1.369698
    I 25>   C      1.036911   -2.124723    2.215329
    I 26>   C      1.895435   -2.668035    3.186206
    I 27>   C      3.083317   -2.013737    3.467470
    I 28>   C      3.399856   -0.816922    2.781193
    I 29>   C     -1.737566    2.058717   -1.726788
    I 30>   C     -2.234269    2.657100   -2.895804
    I 31>   C     -1.822954    2.170682   -4.126369
    I 32>   C     -0.914116    1.087777   -4.174257
    I 33>   C      1.736446   -2.062746   -1.728012
    I 34>   C      2.234462   -2.659281   -2.897424
    I 35>   C      1.824624   -2.170848   -4.127684
    I 36>   C      0.915814   -1.087894   -4.174916
    I 37>   C     -2.049804   -2.465681   -0.433491
    I 38>   C     -1.034112    2.122536    2.216195
    I 39>   C     -3.214997   -3.230418   -0.247505
    I 40>   C     -4.167827   -2.789427    0.655794
    I 41>   C     -3.943830   -1.587369    1.369496
    I 42>   C     -1.892058    2.666935    3.186965
    I 43>   C     -3.080905    2.014270    3.467939
    I 44>   C     -3.398953    0.817967    2.781471
    I 45>   C      0.441990   -0.523293   -5.403715
    I 46>   C     -0.438783    0.525214   -5.403400
    I 47>   C     -4.872873   -1.070288    2.330471
    I 48>   C     -4.608837    0.086400    3.014072
    I 49>   C      4.871150    1.073580    2.330935
    I 50>   C      4.608607   -0.083612    3.014264
    I 51>   H     -1.285955   -2.794672   -1.148155
    I 52>   H     -3.352130   -4.158501   -0.815074
    I 53>   H     -5.089400   -3.361421    0.825026
    I 54>   H     -5.802742   -1.622730    2.514855
    I 55>   H     -5.324945    0.468973    3.752341
    I 56>   H     -3.777935    2.414392    4.216304
    I 57>   H     -1.615547    3.595972    3.699428
    I 58>   H     -0.090529    2.626059    1.972774
    I 59>   H      2.196012   -2.613482   -5.060524
    I 60>   H      0.798347   -0.946694   -6.350950
    I 61>   H     -0.793956    0.950214   -6.350365
    I 62>   H      2.937378   -3.498076   -2.821441
    I 63>   H      2.055069   -2.432675   -0.746963
    I 64>   H     -2.193172    2.614891   -5.058925
    I 65>   H     -2.937300    3.495753   -2.819270
    I 66>   H     -2.057256    2.427150   -0.745533
    I 67>   H      0.093991   -2.629435    1.971734
    I 68>   H      1.620108   -3.597482    3.698555
    I 69>   H      3.780739   -2.412933    4.215961
    I 70>   H      5.325045   -0.465223    3.752708
    I 71>   H      5.800121    1.627401    2.515730
    I 72>   H      5.084749    3.365302    0.825979
    I 73>   H      3.346967    4.159951   -0.814756
    I 74>   H      1.283007    2.792984   -1.148873
    I 75> *
    I 76> 
    I 77> 
    I 78> 
    I 79>                          ****END OF INPUT****
    ================================================================================
        

**Output text.**

```xml
<comment class="example.output" id="input">
       <module cmlx:templateRef="input">
          <module cmlx:templateRef="job">
             <molecule id="initial">
                <atomArray>
                   <atom elementType="C" id="a1" x3="0.0000" y3="0.0000" z3="0.0000">
                      <scalar dataType="" dictRef="cc:basis" />
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="H" id="a2" x3="0.7000" y3="0.5000" z3="0.0000">
                      <scalar dataType="" dictRef="cc:basis" />
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a3" x3="-0.7000" y3="0.5000" z3="0.0000">
                      <scalar dataType="" dictRef="cc:basis" />
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                </atomArray>
                <bondArray>
                   <bond atomRefs2="a1 a2" order="S" />
                   <bond atomRefs2="a1 a3" order="S" />
                </bondArray>
                <formula concise="C 1 H 2">
                   <atomArray count="1 2" elementType="C H" />
                </formula>
                <property dictRef="cml:molmass">
                   <scalar units="unit:dalton">12.0107</scalar>
                </property>
             </molecule>
             <scalar dataType="xsd:integer" dictRef="o:charge">0</scalar>
             <scalar dataType="xsd:integer" dictRef="cc:multiplicity">3</scalar>
             <array dataType="xsd:string" dictRef="cc:keywords" size="3">TZVPP TightSCF mrddci3</array>
             <module cmlx:templateRef="block">
                <scalar dataType="xsd:string" dictRef="o:type">CASSCF</scalar>
                <scalar dataType="xsd:string" dictRef="o:parameters">nel 2</scalar>
                <scalar dataType="xsd:string" dictRef="o:parameter">norb 2</scalar>
                <scalar dataType="xsd:string" dictRef="o:parameter">nevpt2 true</scalar>
             </module>
          </module>
          <module cmlx:templateRef="job">
             <molecule id="initial">
                <atomArray>
                   <atom elementType="C" id="a1" x3="0.0000" y3="0.0000" z3="0.0000">
                      <scalar dataType="" dictRef="cc:basis" />
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="H" id="a2" x3="0.7000" y3="0.5000" z3="0.0000">
                      <scalar dataType="" dictRef="cc:basis" />
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a3" x3="-0.7000" y3="0.5000" z3="0.0000">
                      <scalar dataType="" dictRef="cc:basis" />
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                </atomArray>
                <bondArray>
                   <bond atomRefs2="a1 a2" order="S" />
                   <bond atomRefs2="a1 a3" order="S" />
                </bondArray>
                <formula concise="C 1 H 2">
                   <atomArray count="1 2" elementType="C H" />
                </formula>
                <property dictRef="cml:molmass">
                   <scalar units="unit:dalton">12.0107</scalar>
                </property>
             </molecule>
             <scalar dataType="xsd:integer" dictRef="o:charge">0</scalar>
             <scalar dataType="xsd:integer" dictRef="cc:multiplicity">1</scalar>
             <array dataType="xsd:string" dictRef="cc:keywords" size="3">TZVPP TightSCF mrddci3</array>
             <module cmlx:templateRef="block">
                <scalar dataType="xsd:string" dictRef="o:type">CASSCF</scalar>
                <scalar dataType="xsd:string" dictRef="o:parameters">nel 2</scalar>
                <scalar dataType="xsd:string" dictRef="o:parameter">norb 2</scalar>
                <scalar dataType="xsd:string" dictRef="o:parameter">nevpt2 true</scalar>
             </module>
          </module>
       </module>  
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="input2">
       <module cmlx:templateRef="input">
          <module cmlx:templateRef="job">
             <molecule id="initial">
                <atomArray>
                   <atom elementType="Fe" id="a1" x3="-0.000094" y3="-0.001538" z3="0.015314">
                      <scalar dataType="xsd:string" dictRef="cc:basis">def2-TZVP</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">26</scalar>
                   </atom>
                   <atom elementType="N" id="a2" x3="-1.301044" y3="0.998903" z3="1.550485">
                      <scalar dataType="xsd:string" dictRef="cc:basis">def2-TZVP</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">7</scalar>
                   </atom>
                   <atom elementType="N" id="a3" x3="1.30249" y3="-1.000716" z3="1.549739">
                      <scalar dataType="xsd:string" dictRef="cc:basis">def2-TZVP</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">7</scalar>
                   </atom>
                   <atom elementType="N" id="a4" x3="0.877835" y3="-1.039833" z3="-1.73239">
                      <scalar dataType="xsd:string" dictRef="cc:basis">def2-TZVP</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">7</scalar>
                   </atom>
                   <atom elementType="N" id="a5" x3="1.803903" y3="1.327699" z3="0.218253">
                      <scalar dataType="xsd:string" dictRef="cc:basis">def2-TZVP</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">7</scalar>
                   </atom>
                   <atom elementType="N" id="a6" x3="-1.805188" y3="-1.32875" z3="0.218929">
                      <scalar dataType="xsd:string" dictRef="cc:basis">def2-TZVP</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">7</scalar>
                   </atom>
                   <atom elementType="N" id="a7" x3="-0.878918" y3="1.035806" z3="-1.73179">
                      <scalar dataType="xsd:string" dictRef="cc:basis">def2-TZVP</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">7</scalar>
                   </atom>
                   <atom elementType="C" id="a8" x3="2.460016" y3="-0.340681" z3="1.821585">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a9" x3="2.730294" y3="0.885483" z3="1.110808">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a10" x3="-2.731299" y3="-0.885256" z3="1.111155">
                      <scalar dataType="xsd:string" dictRef="cc:basis">def2-TZVP</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a11" x3="-2.459525" y3="0.340464" z3="1.822082">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a12" x3="0.463935" y3="-0.550934" z3="-2.934373">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a13" x3="-0.46369" y3="0.548788" z3="-2.934056">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a14" x3="2.047074" y3="2.465059" z3="-0.433956">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a15" x3="3.211011" y3="3.231578" z3="-0.247375">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a16" x3="4.16413" y3="2.791912" z3="0.656265">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a17" x3="3.941678" y3="1.589394" z3="1.369698">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a18" x3="1.036911" y3="-2.124723" z3="2.215329">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a19" x3="1.895435" y3="-2.668035" z3="3.186206">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a20" x3="3.083317" y3="-2.013737" z3="3.46747">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a21" x3="3.399856" y3="-0.816922" z3="2.781193">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a22" x3="-1.737566" y3="2.058717" z3="-1.726788">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a23" x3="-2.234269" y3="2.6571" z3="-2.895804">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a24" x3="-1.822954" y3="2.170682" z3="-4.126369">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a25" x3="-0.914116" y3="1.087777" z3="-4.174257">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a26" x3="1.736446" y3="-2.062746" z3="-1.728012">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a27" x3="2.234462" y3="-2.659281" z3="-2.897424">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a28" x3="1.824624" y3="-2.170848" z3="-4.127684">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a29" x3="0.915814" y3="-1.087894" z3="-4.174916">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a30" x3="-2.049804" y3="-2.465681" z3="-0.433491">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a31" x3="-1.034112" y3="2.122536" z3="2.216195">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a32" x3="-3.214997" y3="-3.230418" z3="-0.247505">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a33" x3="-4.167827" y3="-2.789427" z3="0.655794">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a34" x3="-3.94383" y3="-1.587369" z3="1.369496">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a35" x3="-1.892058" y3="2.666935" z3="3.186965">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a36" x3="-3.080905" y3="2.01427" z3="3.467939">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a37" x3="-3.398953" y3="0.817967" z3="2.781471">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a38" x3="0.44199" y3="-0.523293" z3="-5.403715">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a39" x3="-0.438783" y3="0.525214" z3="-5.4034">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a40" x3="-4.872873" y3="-1.070288" z3="2.330471">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a41" x3="-4.608837" y3="0.0864" z3="3.014072">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a42" x3="4.87115" y3="1.07358" z3="2.330935">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="C" id="a43" x3="4.608607" y3="-0.083612" z3="3.014264">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">6</scalar>
                   </atom>
                   <atom elementType="H" id="a44" x3="-1.285955" y3="-2.794672" z3="-1.148155">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a45" x3="-3.35213" y3="-4.158501" z3="-0.815074">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a46" x3="-5.0894" y3="-3.361421" z3="0.825026">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a47" x3="-5.802742" y3="-1.62273" z3="2.514855">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a48" x3="-5.324945" y3="0.468973" z3="3.752341">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a49" x3="-3.777935" y3="2.414392" z3="4.216304">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a50" x3="-1.615547" y3="3.595972" z3="3.699428">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a51" x3="-0.090529" y3="2.626059" z3="1.972774">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a52" x3="2.196012" y3="-2.613482" z3="-5.060524">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a53" x3="0.798347" y3="-0.946694" z3="-6.35095">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a54" x3="-0.793956" y3="0.950214" z3="-6.350365">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a55" x3="2.937378" y3="-3.498076" z3="-2.821441">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a56" x3="2.055069" y3="-2.432675" z3="-0.746963">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a57" x3="-2.193172" y3="2.614891" z3="-5.058925">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a58" x3="-2.9373" y3="3.495753" z3="-2.81927">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a59" x3="-2.057256" y3="2.42715" z3="-0.745533">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a60" x3="0.093991" y3="-2.629435" z3="1.971734">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a61" x3="1.620108" y3="-3.597482" z3="3.698555">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a62" x3="3.780739" y3="-2.412933" z3="4.215961">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a63" x3="5.325045" y3="-0.465223" z3="3.752708">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a64" x3="5.800121" y3="1.627401" z3="2.51573">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a65" x3="5.084749" y3="3.365302" z3="0.825979">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a66" x3="3.346967" y3="4.159951" z3="-0.814756">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                   <atom elementType="H" id="a67" x3="1.283007" y3="2.792984" z3="-1.148873">
                      <scalar dataType="xsd:string" dictRef="cc:basis">N/A</scalar>
                      <scalar dataType="xsd:integer" dictRef="cc:atomicNumber">1</scalar>
                   </atom>
                </atomArray>
                <bondArray>
                   <bond atomRefs2="a2 a11" order="S" />
                   <bond atomRefs2="a2 a31" order="S" />
                   <bond atomRefs2="a3 a8" order="S" />
                   <bond atomRefs2="a3 a18" order="S" />
                   <bond atomRefs2="a4 a12" order="S" />
                   <bond atomRefs2="a4 a26" order="S" />
                   <bond atomRefs2="a5 a9" order="S" />
                   <bond atomRefs2="a5 a14" order="S" />
                   <bond atomRefs2="a6 a10" order="S" />
                   <bond atomRefs2="a6 a30" order="S" />
                   <bond atomRefs2="a7 a13" order="S" />
                   <bond atomRefs2="a7 a22" order="S" />
                   <bond atomRefs2="a8 a9" order="S" />
                   <bond atomRefs2="a8 a21" order="S" />
                   <bond atomRefs2="a9 a17" order="S" />
                   <bond atomRefs2="a10 a11" order="S" />
                   <bond atomRefs2="a10 a34" order="S" />
                   <bond atomRefs2="a11 a37" order="S" />
                   <bond atomRefs2="a12 a13" order="S" />
                   <bond atomRefs2="a12 a29" order="S" />
                   <bond atomRefs2="a13 a25" order="S" />
                   <bond atomRefs2="a14 a15" order="S" />
                   <bond atomRefs2="a14 a67" order="S" />
                   <bond atomRefs2="a15 a16" order="S" />
                   <bond atomRefs2="a15 a66" order="S" />
                   <bond atomRefs2="a16 a17" order="S" />
                   <bond atomRefs2="a16 a65" order="S" />
                   <bond atomRefs2="a17 a42" order="S" />
                   <bond atomRefs2="a18 a19" order="S" />
                   <bond atomRefs2="a18 a60" order="S" />
                   <bond atomRefs2="a19 a20" order="S" />
                   <bond atomRefs2="a19 a61" order="S" />
                   <bond atomRefs2="a20 a21" order="S" />
                   <bond atomRefs2="a20 a62" order="S" />
                   <bond atomRefs2="a21 a43" order="S" />
                   <bond atomRefs2="a22 a23" order="S" />
                   <bond atomRefs2="a22 a59" order="S" />
                   <bond atomRefs2="a23 a24" order="S" />
                   <bond atomRefs2="a23 a58" order="S" />
                   <bond atomRefs2="a24 a25" order="S" />
                   <bond atomRefs2="a24 a57" order="S" />
                   <bond atomRefs2="a25 a39" order="S" />
                   <bond atomRefs2="a26 a27" order="S" />
                   <bond atomRefs2="a26 a56" order="S" />
                   <bond atomRefs2="a27 a28" order="S" />
                   <bond atomRefs2="a27 a55" order="S" />
                   <bond atomRefs2="a28 a29" order="S" />
                   <bond atomRefs2="a28 a52" order="S" />
                   <bond atomRefs2="a29 a38" order="S" />
                   <bond atomRefs2="a30 a32" order="S" />
                   <bond atomRefs2="a30 a44" order="S" />
                   <bond atomRefs2="a31 a35" order="S" />
                   <bond atomRefs2="a31 a51" order="S" />
                   <bond atomRefs2="a32 a33" order="S" />
                   <bond atomRefs2="a32 a45" order="S" />
                   <bond atomRefs2="a33 a34" order="S" />
                   <bond atomRefs2="a33 a46" order="S" />
                   <bond atomRefs2="a34 a40" order="S" />
                   <bond atomRefs2="a35 a36" order="S" />
                   <bond atomRefs2="a35 a50" order="S" />
                   <bond atomRefs2="a36 a37" order="S" />
                   <bond atomRefs2="a36 a49" order="S" />
                   <bond atomRefs2="a37 a41" order="S" />
                   <bond atomRefs2="a38 a39" order="S" />
                   <bond atomRefs2="a38 a53" order="S" />
                   <bond atomRefs2="a39 a54" order="S" />
                   <bond atomRefs2="a40 a41" order="S" />
                   <bond atomRefs2="a40 a47" order="S" />
                   <bond atomRefs2="a41 a48" order="S" />
                   <bond atomRefs2="a42 a43" order="S" />
                   <bond atomRefs2="a42 a64" order="S" />
                   <bond atomRefs2="a43 a63" order="S" />
                </bondArray>
                <formula concise="C 36 H 24 Fe 1 N 6">
                   <atomArray count="36 24 1 6" elementType="C H Fe N" />
                </formula>
                <property dictRef="cml:molmass">
                   <scalar units="unit:dalton">572.2703999999998</scalar>
                </property>
             </molecule>
             <scalar dataType="xsd:integer" dictRef="o:charge">2</scalar>
             <scalar dataType="xsd:integer" dictRef="cc:multiplicity">5</scalar>
             <array dataType="xsd:string" dictRef="cc:keywords" size="6">OPBE opt def2-SV(P) def2-SVP/C TightSCF UNO</array>
             <module cmlx:templateRef="block">
                <scalar dataType="xsd:string" dictRef="o:type">output</scalar>
                <scalar dataType="xsd:string" dictRef="o:parameters" />
                <scalar dataType="xsd:string" dictRef="o:parameter">Print[ P_UNO_OccNum ] = 1</scalar>
             </module>
          </module>
       </module>  
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="input3">
        <module cmlx:templateRef="input">
           <module cmlx:templateRef="job">
              <array dataType="xsd:string" dictRef="cc:keywords" size="4">HF def2-SVP TightSCF Opt</array>
              <module cmlx:templateRef="block">
                 <scalar dataType="xsd:string" dictRef="o:type">PAL</scalar>
                 <scalar dataType="xsd:string" dictRef="o:parameters">NPROCS 1 END</scalar>
              </module>
              <module cmlx:templateRef="block">
                 <scalar dataType="xsd:string" dictRef="o:type">geom</scalar>
                 <scalar dataType="xsd:string" dictRef="o:parameters">Constraints</scalar>
                 <scalar dataType="xsd:string" dictRef="o:parameter">{ A 1 0 2 90.0 C}</scalar>
              </module>
              <module cmlx:templateRef="basis">
                 <array dataType="xsd:string" dictRef="o:basisparameter" size="3">%basis basis SV</array>
                 <array dataType="xsd:string" dictRef="o:basisparameter" size="4">newGTO O "6-31G" end</array>
                 <array dataType="xsd:string" dictRef="o:basisparameter" size="1">end</array>
              </module>
              <scalar dataType="xsd:integer" dictRef="o:charge">0</scalar>
              <scalar dataType="xsd:integer" dictRef="cc:multiplicity">1</scalar>
           </module>
        </module> 
    </comment>
```
