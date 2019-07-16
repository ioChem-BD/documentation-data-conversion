# logfile {#logfile-d3e4306}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | ADF log                                                                                                                                                                                               |
| id                                                                                                                                                                                                    | logfile                                                                                                                                                                                               |
| name                                                                                                                                                                                                  | Final log file resume                                                                                                                                                                                 |
| pattern                                                                                                                                                                                               | \\s\*\\(LOGFILE\\).\*                                                                                                                                                                                 |
| endPattern                                                                                                                                                                                            | .\*END.\*\$(.(?!:))\*                                                                                                                                                                                 |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | logfile.xml                                                                                                                                                                                           |

######Template attributes

**Input.**

            
                (LOGFILE)
             <May04-2010> <06:12:25>  END
             <May04-2010> <06:12:26>  ADF 2009.01  RunTime: May04-2010 06:12:26
             <May04-2010> <06:12:26>  OPT C80BUTPROD69 CONT 12
             <May04-2010> <06:12:27>  RunType   : SINGLE POINT
             <May04-2010> <06:12:27>  Net Charge: 0 (Nuclei minus Electrons)
             <May04-2010> <06:12:27>  Symmetry  : NOSYM
             <May04-2010> <06:12:27>  >>>> FRAGM
             <May04-2010> <06:12:28>  >>>> CORORT
             <May04-2010> <06:12:29>  >>>> FITINT
             <May04-2010> <06:12:35>  >>>> CLSMAT
             <May04-2010> <06:12:35>  >>>> ORTHON
             <May04-2010> <06:12:40>  >>>> GENPT
             <May04-2010> <06:12:41>  Acc.Num.Int.=   6.000
             <May04-2010> <06:12:42>  Block Length= 128
             <May04-2010> <06:12:48>  >>>> PTBAS
             <May04-2010> <06:15:28>  >>>> CYCLE
             <May04-2010> <06:15:50>    1
             <May04-2010> <06:16:33>    2  ErrMat   2.79814121  MaxEl  0.48176486
             <May04-2010> <06:17:06>    3  ErrMat   1.51224955  MaxEl  0.09978819
             <May04-2010> <06:17:39>    4  ErrMat   0.94765889  MaxEl -0.04486329
             <May04-2010> <06:18:25>    5  ErrMat   0.61366968  MaxEl  0.04137339
             <May04-2010> <06:18:59>    6  ErrMat   0.63098527  MaxEl  0.09804162
             <May04-2010> <06:19:32>    7  ErrMat   0.22216777  MaxEl  0.03069437
             <May04-2010> <06:20:05>    8  ErrMat   0.09119102  MaxEl -0.01194218
             <May04-2010> <06:20:37>    9  ErrMat   0.08555816  MaxEl  0.00727754
             <May04-2010> <06:21:10>   10  ErrMat   0.03727656  MaxEl -0.00234168
             <May04-2010> <06:21:44>   11  ErrMat   0.01712033  MaxEl  0.00302702
             <May04-2010> <06:22:17>   12  ErrMat   0.00478966  MaxEl -0.00038518
             <May04-2010> <06:22:49>   13  ErrMat   0.00736128  MaxEl -0.00097317
             <May04-2010> <06:23:22>   14  ErrMat   0.00303646  MaxEl  0.00049233
             <May04-2010> <06:23:55>   15  ErrMat   0.00100783  MaxEl -0.00014174
             <May04-2010> <06:24:27>   16  ErrMat   0.00043373  MaxEl  0.00006704
             <May04-2010> <06:25:01>   17  ErrMat   0.00027019  MaxEl -0.00002004
             <May04-2010> <06:25:35>   18  ErrMat   0.00007548  MaxEl -0.00000797
             <May04-2010> <06:26:08>   19  ErrMat   0.00008791  MaxEl -0.00001188
             <May04-2010> <06:26:41>   20  ErrMat   0.00002641  MaxEl  0.00000333
             <May04-2010> <06:27:14>   21  ErrMat   0.00000780  MaxEl -0.00000057
             <May04-2010> <06:27:20>  SCF converged
             <May04-2010> <06:27:47>   22  ErrMat   0.00001758  MaxEl -0.00000151
             <May04-2010> <06:28:12>  >>>> TOTEN
             <May04-2010> <06:36:34>  >>>> POPAN
             <May04-2010> <06:36:34>  >>>> DEBYE
             <May04-2010> <06:36:37>  >>>> AMETS
             <May04-2010> <06:36:43>   Bond Energy LDA     -31.82018839 a.u.
             <May04-2010> <06:36:43>   Bond Energy LDA    -865.87138203 eV
             <May04-2010> <06:36:43>           + GGA-X     -25.93787799 a.u.
             <May04-2010> <06:36:43>           + GGA-X    -705.80557174 eV
             <May04-2010> <06:36:43>          + GGA-XC     -28.47073192 a.u.
             <May04-2010> <06:36:43>          + GGA-XC    -774.72803397 eV
             <May04-2010> <06:36:43>  >>>> POPUL
             <May04-2010> <06:36:49>  NORMAL TERMINATION
             <May04-2010> <06:36:51>  END
                     
             
        

**Output text.**

```xml
<comment class="example.output" id="logfile">
        <module cmlx:lineCount="53" cmlx:templateRef="logfile">
            <scalar dataType="xsd:string" dictRef="cc:runDate">May04-2010 06:12:26</scalar>
            <scalar dataType="xsd:integer" dictRef="a:charge">0</scalar>
            <scalar dataType="xsd:double" dictRef="cc:potentialEnergy" units="nonsi:electronvolt">-774.72803397</scalar>
        </module>
    </comment>
```