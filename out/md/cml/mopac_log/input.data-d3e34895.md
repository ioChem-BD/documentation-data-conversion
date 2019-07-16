# input.data {#input.data-d3e34895}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | MOPAC log                                                                                                                                                                                             |
| id                                                                                                                                                                                                    | input.data                                                                                                                                                                                            |
| name                                                                                                                                                                                                  | Input data section                                                                                                                                                                                    |
| pattern                                                                                                                                                                                               | \\s\*\\\#{10,}\\s\*\$\\s\*\\\#\\s+\\\#\\s\*\$\\s\*\\\#\\s\*Start\\sof\\sInput\\sdata\\s\*\\\#\\s\*                                                                                                    |
| endPattern                                                                                                                                                                                            | (?!\\s\*\\\#+).\*\$\\s\*\\\#{10,}\\s\*                                                                                                                                                                |
| endPattern2                                                                                                                                                                                           | (?!\\s\*\\\*+).\*\$\\s\*\\\*{10,}                                                                                                                                                                     |
| endPattern3                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| offset                                                                                                                                                                                                | 1                                                                                                                                                                                                     |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | input.data.xml                                                                                                                                                                                        |

######Template attributes

**Input.**

     ####################################
     #                                  #
     #       Start of Input data        #
     #                                  #
     ####################################
     MOPAC_VERSION=MOPAC2016.16.041 
     DATE="Tue Feb 26 17:21:22 2019"
     METHOD=PM7
     TITLE="Coordinates generated by ADFinput (c) SCM 1998-2011"
     KEYWORDS=" PM7 GEO-OK FORCE LET NOREOR AUX(0,PRECISION=9) BONDS CHARGE=0"
     COMMENTS=""
     ATOM_EL[014]=
      O  C  H  C  H  H  O  H  C  C  O  H  H  O 
     ATOM_CORE[014]=
      6  4  1  4  1  1  6  1  4  4  6  1  1  6 
     ATOM_X:ANGSTROMS[042]=
        4.8790953800000    6.8880495400000    3.5648869000000
        3.7138746600000    6.9103490400000    2.6514257900000
        4.5022436300000    7.2699278600000    4.4734766200000
        2.6452997300000    6.1107610300000    3.3142558000000
        4.0984309700000    6.4873019700000    1.7158946600000
        3.4791670300000    7.9986289800000    2.4886888400000
        0.4511955600000    1.2331308600000    2.9221720800000
        2.9411642700000    5.5277664100000    4.1552267900000
        1.2211612100000    6.5282494100000    3.0699877400000
        1.5406063900000    1.5763933300000    2.6369151000000
        1.7241128600000    5.3133201900000    2.4142533200000
        0.5226132100000    6.1341378500000    3.8105266900000
        0.8354992600000    7.3426486200000    2.4263760900000
        2.5887558500000    1.9395349200000    2.2598835900000
     AO_ATOMINDEX[038]=
      1  1  1  1  2  2  2  2  3  4  4  4  4  5  6  7  7  7  7  8  9  9  9  9 10 10 10 10 11 11 11 11 12 13 14 14 14 14
     ATOM_SYMTYPE[038]=
      S PX PY PZ  S PX PY PZ  S  S PX PY PZ  S  S  S PX PY PZ  S  S PX PY PZ  S PX PY PZ  S PX PY PZ  S  S  S PX PY PZ 
     AO_ZETA[038]=
      5.9723090000000  2.3490170000000  2.3490170000000  2.3490170000000  1.9422440000000  1.7087230000000  1.7087230000000  1.7087230000000  1.2602370000000  1.9422440000000
      1.7087230000000  1.7087230000000  1.7087230000000  1.2602370000000  1.2602370000000  5.9723090000000  2.3490170000000  2.3490170000000  2.3490170000000  1.2602370000000
      1.9422440000000  1.7087230000000  1.7087230000000  1.7087230000000  1.9422440000000  1.7087230000000  1.7087230000000  1.7087230000000  5.9723090000000  2.3490170000000
      2.3490170000000  2.3490170000000  1.2602370000000  1.2602370000000  5.9723090000000  2.3490170000000  2.3490170000000  2.3490170000000
     ATOM_PQN[038]=
     2 2 2 2 2 2 2 2 1 2 2 2 2 1 1 2 2 2 2 1 2 2 2 2 2 2 2 2 2 2 2 2 1 1 2 2 2 2
     NUM_ELECTRONS=046
     EMPIRICAL_FORMULA="C4 H6 O4  =    14 atoms"
     ####################################
        

**Output text.**

```xml
<comment class="example.output" id="input.data">
        <module cmlx:templateRef="input.data">
          <list cmlx:templateRef="missingID" />
          <list cmlx:templateRef="lines">
             <scalar dataType="xsd:string" dictRef="mp:input.data">MOPAC_VERSION=MOPAC2016.16.041</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">DATE="Tue Feb 26 17:21:22 2019"</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">METHOD=PM7</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">TITLE="Coordinates generated by ADFinput (c) SCM 1998-2011"</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">KEYWORDS=" PM7 GEO-OK FORCE LET NOREOR AUX(0,PRECISION=9) BONDS CHARGE=0"</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">COMMENTS=""</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">ATOM_EL[014]=</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">O  C  H  C  H  H  O  H  C  C  O  H  H  O</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">ATOM_CORE[014]=</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">6  4  1  4  1  1  6  1  4  4  6  1  1  6</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">ATOM_X:ANGSTROMS[042]=</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">4.8790953800000    6.8880495400000    3.5648869000000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">3.7138746600000    6.9103490400000    2.6514257900000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">4.5022436300000    7.2699278600000    4.4734766200000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">2.6452997300000    6.1107610300000    3.3142558000000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">4.0984309700000    6.4873019700000    1.7158946600000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">3.4791670300000    7.9986289800000    2.4886888400000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">0.4511955600000    1.2331308600000    2.9221720800000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">2.9411642700000    5.5277664100000    4.1552267900000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">1.2211612100000    6.5282494100000    3.0699877400000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">1.5406063900000    1.5763933300000    2.6369151000000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">1.7241128600000    5.3133201900000    2.4142533200000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">0.5226132100000    6.1341378500000    3.8105266900000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">0.8354992600000    7.3426486200000    2.4263760900000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">2.5887558500000    1.9395349200000    2.2598835900000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">AO_ATOMINDEX[038]=</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">1  1  1  1  2  2  2  2  3  4  4  4  4  5  6  7  7  7  7  8  9  9  9  9 10 10 10 10 11 11 11 11 12 13 14 14 14 14</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">ATOM_SYMTYPE[038]=</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">S PX PY PZ  S PX PY PZ  S  S PX PY PZ  S  S  S PX PY PZ  S  S PX PY PZ  S PX PY PZ  S PX PY PZ  S  S  S PX PY PZ</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">AO_ZETA[038]=</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">5.9723090000000  2.3490170000000  2.3490170000000  2.3490170000000  1.9422440000000  1.7087230000000  1.7087230000000  1.7087230000000  1.2602370000000  1.9422440000000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">1.7087230000000  1.7087230000000  1.7087230000000  1.2602370000000  1.2602370000000  5.9723090000000  2.3490170000000  2.3490170000000  2.3490170000000  1.2602370000000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">1.9422440000000  1.7087230000000  1.7087230000000  1.7087230000000  1.9422440000000  1.7087230000000  1.7087230000000  1.7087230000000  5.9723090000000  2.3490170000000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">2.3490170000000  2.3490170000000  1.2602370000000  1.2602370000000  5.9723090000000  2.3490170000000  2.3490170000000  2.3490170000000</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">ATOM_PQN[038]=</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">2 2 2 2 2 2 2 2 1 2 2 2 2 1 1 2 2 2 2 1 2 2 2 2 2 2 2 2 2 2 2 2 1 1 2 2 2 2</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">NUM_ELECTRONS=046</scalar>
             <scalar dataType="xsd:string" dictRef="mp:input.data">EMPIRICAL_FORMULA="C4 H6 O4  =    14 atoms"</scalar>
          </list>
        </module>
    </comment>
```