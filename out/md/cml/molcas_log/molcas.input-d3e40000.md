# molcas.input {#molcas.input-d3e40000}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | MOLCAS input                                                                                                                                                                                          |
| id                                                                                                                                                                                                    | molcas.input                                                                                                                                                                                          |
| name                                                                                                                                                                                                  | MOLCAS input                                                                                                                                                                                          |
| xml:base                                                                                                                                                                                              | topTemplate.xml                                                                                                                                                                                       |

######Template attributes

**Comment.**

    > DO WHILE

     &SEWARD &END
    Symmetry
     Y XYZ
    Basis set
    C.ano-s...4s3p1d.
    C   0.73915685  0.00000000 -0.19129462  Angstrom
    End of Basis
    Basis set
    H.ano-s...2s1p.
    H1  1.37322192  0.00000000  0.69209432  Angstrom
    H2  0.99210112  0.87816821 -0.78047182  Angstrom
    End of Basis
    End of Input

     &RASSCF &END
    Nactel
     6 0 0
    Inactive
     2 0 3 1
    RAS2
     3 1 2 1
    End of Input

     &CASPT2 &END
    End of Input

     &SLAPAF &END
    End of Input

    > END DO

     &MCKINLEY &END
    End of Input
        
        

**Output text.**

```xml
<comment class="example.output" id="molcas.input">
      <module id="molcas.input">
         <module cmlx:templateRef="basis">
            <array delimiter="I" dictRef="m:basis1" size="7">CIano-sIII4s3p1dII</array>
            <list>
               <scalar dataType="xsd:string" dictRef="m:label">C</scalar>
               <scalar dataType="xsd:double" dictRef="cc:x3">0.73915685</scalar>
               <scalar dataType="xsd:double" dictRef="cc:y3">0.00000000</scalar>
               <scalar dataType="xsd:double" dictRef="cc:z3">-0.19129462</scalar>
            </list>
         </module>
         <module cmlx:templateRef="basis">
            <array delimiter="I" dictRef="m:basis1" size="7">HIano-sIII2s1pII</array>
            <list>
               <scalar dataType="xsd:string" dictRef="m:label">H1</scalar>
               <scalar dataType="xsd:double" dictRef="cc:x3">1.37322192</scalar>
               <scalar dataType="xsd:double" dictRef="cc:y3">0.00000000</scalar>
               <scalar dataType="xsd:double" dictRef="cc:z3">0.69209432</scalar>
            </list>
            <list>
               <scalar dataType="xsd:string" dictRef="m:label">H2</scalar>
               <scalar dataType="xsd:double" dictRef="cc:x3">0.99210112</scalar>
               <scalar dataType="xsd:double" dictRef="cc:y3">0.87816821</scalar>
               <scalar dataType="xsd:double" dictRef="cc:z3">-0.78047182</scalar>
            </list>
         </module>
         <map id="atomTypeLabels">
            <link from="C" to="C" />
            <link from="C" to="C" />
            <link from="H1" to="H" />
            <link from="H2" to="H" />
            <link from="H2" to="H" />
         </map>
         <module dictRef="unprocessed">
            <scalar dataType="xsd:string" dictRef="m:inputline">> DO WHILE</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline" />
            <scalar dataType="xsd:string" dictRef="m:inputline">&SEWARD &END</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">Symmetry</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">Y XYZ</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">End of Input</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline" />
            <scalar dataType="xsd:string" dictRef="m:inputline">&RASSCF &END</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">Nactel</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">6 0 0</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">Inactive</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">2 0 3 1</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">RAS2</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">3 1 2 1</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">End of Input</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline" />
            <scalar dataType="xsd:string" dictRef="m:inputline">&CASPT2 &END</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">End of Input</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline" />
            <scalar dataType="xsd:string" dictRef="m:inputline">&SLAPAF &END</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">End of Input</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline" />
            <scalar dataType="xsd:string" dictRef="m:inputline">> END DO</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline" />
            <scalar dataType="xsd:string" dictRef="m:inputline">&MCKINLEY &END</scalar>
            <scalar dataType="xsd:string" dictRef="m:inputline">End of Input</scalar>
         </module>
      </module>
    </comment>
```
