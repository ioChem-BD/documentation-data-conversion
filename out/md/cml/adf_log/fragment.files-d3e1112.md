# fragment.files {#fragment.files-d3e1112}

ADF log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | fragment.files                                                                                                                                      |
| name                                                                                                                                                | Fragment files section                                                                                                                              |
| pattern                                                                                                                                             | \\s+Fragment\\sFile\\(s\\).\*                                                                                                                       |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | fragment.files.xml                                                                                                                                  |

######Template attributes

**Input.**

     Fragment File(s)
     ----------------
     Lu:
             file : t21.Lu.5p
             jobid: ADF 2012.01  RunTime: Nov11-2013 11:30:15  Nodes: 1  Procs: 1
             title: Lutetium (TZP, 5p frozen)
     N:
             file : t21.N.1s
             jobid: ADF 2012.01  RunTime: Nov11-2013 11:30:16  Nodes: 1  Procs: 1
             title: Nitrogen (TZP, 1s frozen)
     H:
             file : t21.H
             jobid: ADF 2012.01  RunTime: Nov11-2013 11:30:17  Nodes: 1  Procs: 1
             title: Hydrogen (TZP)
     C:
             file : t21.C.1s
             jobid: ADF 2012.01  RunTime: Nov11-2013 11:30:16  Nodes: 1  Procs: 1
             title: Carbon (TZP, 1s frozen)

        

**Input.**

     Fragment File(s)
     ----------------
     W:
             file : t21.W.4d
             jobid: ADF 2007.01  RunTime: Oct16-2008 12:08:13
             title: Tungsten (TZP, 4d frozen)
     V:
             file : t21.V.2p
             jobid: ADF 2007.01  RunTime: Oct16-2008 12:08:14
             title: Vanadium (TZP, 2p frozen)
     O:
             file : t21.O.1s
             jobid: ADF 2007.01  RunTime: Oct16-2008 12:08:12
             title: Oxygen (TZP, 1s frozen)

        

**Output text.**

```xml
<comment class="example.output" id="fragment.files">
        <module cmlx:lineCount="18" cmlx:templateRef="fragment.files">
            <module cmlx:lineCount="18" cmlx:templateRef="fragment.files">
              <list cmlx:templateRef="elementType">
                <atom elementType="Lu" id="a1">
                  <scalar dataType="xsd:string" dictRef="a:file">t21.Lu.5p</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:jobname">ADF 2012.01</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:runtime">Nov11-2013 11:30:15</scalar>
                  <scalar dataType="xsd:integer" dictRef="cc:nodes">1</scalar>
                  <scalar dataType="xsd:integer" dictRef="cc:processors">1</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:elementName">Lutetium</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:basis">TZP</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:contraction">5p</scalar>
                </atom>
              </list>
            </module>
            <module cmlx:lineCount="4" cmlx:templateRef="atom">
              <list cmlx:templateRef="elementType">
                <atom elementType="N" id="a1">
                  <scalar dataType="xsd:string" dictRef="a:file">t21.N.1s</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:jobname">ADF 2012.01</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:runtime">Nov11-2013 11:30:16</scalar>
                  <scalar dataType="xsd:integer" dictRef="cc:nodes">1</scalar>
                  <scalar dataType="xsd:integer" dictRef="cc:processors">1</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:elementName">Nitrogen</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:basis">TZP</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:contraction">1s</scalar>
                </atom>
              </list>
            </module>
            <module cmlx:lineCount="4" cmlx:templateRef="atom">
              <list cmlx:templateRef="elementType">
                <atom elementType="H" id="a1">
                  <scalar dataType="xsd:string" dictRef="a:file">t21.H</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:jobname">ADF 2012.01</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:runtime">Nov11-2013 11:30:17</scalar>
                  <scalar dataType="xsd:integer" dictRef="cc:nodes">1</scalar>
                  <scalar dataType="xsd:integer" dictRef="cc:processors">1</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:elementName">Hydrogen</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:basis">TZP</scalar>
                </atom>
              </list>
            </module>
            <module cmlx:lineCount="4" cmlx:templateRef="atom">
              <list cmlx:templateRef="elementType">
                <atom elementType="C" id="a1">
                  <scalar dataType="xsd:string" dictRef="a:file">t21.C.1s</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:jobname">ADF 2012.01</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:runtime">Nov11-2013 11:30:16</scalar>
                  <scalar dataType="xsd:integer" dictRef="cc:nodes">1</scalar>
                  <scalar dataType="xsd:integer" dictRef="cc:processors">1</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:elementName">Carbon</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:basis">TZP</scalar>
                  <scalar dataType="xsd:string" dictRef="cc:contraction">1s</scalar>
                </atom>
              </list>
            </module>
          </module>   
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="fragment.files2">
        <module cmlx:lineCount="14" cmlx:templateRef="fragment.files">
          <module cmlx:lineCount="4" cmlx:templateRef="atom">
           <list cmlx:templateRef="elementType">
            <atom elementType="W" id="a1">
             <scalar dataType="xsd:string" dictRef="a:file">t21.W.4d</scalar>
             <scalar dataType="xsd:string" dictRef="cc:jobname">ADF 2007.01</scalar>
             <scalar dataType="xsd:string" dictRef="cc:runtime">Oct16-2008 12:08:13</scalar>
             <scalar dataType="xsd:string" dictRef="cc:elementName">Tungsten</scalar>
             <scalar dataType="xsd:string" dictRef="cc:basis">TZP</scalar>
             <scalar dataType="xsd:string" dictRef="cc:contraction">4d</scalar>
            </atom>
           </list>
          </module>
          <module cmlx:lineCount="4" cmlx:templateRef="atom">
           <list cmlx:templateRef="elementType">
            <atom elementType="V" id="a1">
             <scalar dataType="xsd:string" dictRef="a:file">t21.V.2p</scalar>
             <scalar dataType="xsd:string" dictRef="cc:jobname">ADF 2007.01</scalar>
             <scalar dataType="xsd:string" dictRef="cc:runtime">Oct16-2008 12:08:14</scalar>
             <scalar dataType="xsd:string" dictRef="cc:elementName">Vanadium</scalar>
             <scalar dataType="xsd:string" dictRef="cc:basis">TZP</scalar>
             <scalar dataType="xsd:string" dictRef="cc:contraction">2p</scalar>
            </atom>
           </list>
          </module>
          <module cmlx:lineCount="4" cmlx:templateRef="atom">
           <list cmlx:templateRef="elementType">
            <atom elementType="O" id="a1">
             <scalar dataType="xsd:string" dictRef="a:file">t21.O.1s</scalar>
             <scalar dataType="xsd:string" dictRef="cc:jobname">ADF 2007.01</scalar>
             <scalar dataType="xsd:string" dictRef="cc:runtime">Oct16-2008 12:08:12</scalar>
             <scalar dataType="xsd:string" dictRef="cc:elementName">Oxygen</scalar>
             <scalar dataType="xsd:string" dictRef="cc:basis">TZP</scalar>
             <scalar dataType="xsd:string" dictRef="cc:contraction">1s</scalar>
            </atom>
           </list>
          </module>
         </module>
    </comment>
```
