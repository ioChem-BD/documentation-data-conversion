# basisset {#basisset-d3e24211}

Turbomole log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole log                                                                                                                                                                                         |
| id                                                                                                                                                                                                    | basisset                                                                                                                                                                                              |
| name                                                                                                                                                                                                  | Basis set information section                                                                                                                                                                         |
| pattern                                                                                                                                                                                               | \\s\*\\+\\-+\\+\\s\*\$\\s\*\\I\\s\*basis\\sset\\sinformation\\s\*\\I\\s\*\$\\s\*\\+\\-+\\+\\s\*                                                                                                       |
| endPattern                                                                                                                                                                                            | \\s\*total\\snumber\\sof\\sSCF-basis\\sfunctions.\*                                                                                                                                                   |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | basisset.xml                                                                                                                                                                                          |

######Template attributes

**Input.**

                  +--------------------------------------------------+
                  I               basis set information              I
                  +--------------------------------------------------+


                  we will work with the  1s 3p 5d  7f  9g ... basis set
                  ...i.e. with spherical basis functions...


       type   atoms  prim   cont   basis
       ---------------------------------------------------------------------------
        c       82     25     15   DZP   [4s2p1dI8s4p1d]
        sc       2     92     45   def2-TZVP   [6s4p4d1fI17s11p7d1f]
       ---------------------------------------------------------------------------
       total:   84   2234   1320
       ---------------------------------------------------------------------------

       total number of primitive shells          :   49
       total number of contracted shells         :  604
       total number of cartesian basis functions : 1416
       total number of SCF-basis functions       : 1320 
        

**Output text.**

```xml
<comment class="example.output" id="basisset">
        <module cmlx:lineCount="20" cmlx:templateRef="basisset">
            <list cmlx:lineCount="2" cmlx:templateRef="basis">
               <array dataType="xsd:string" dictRef="cc:atomType" size="2">c sc</array>
               <array dataType="xsd:integer" dictRef="t:atoms" size="2">82 2</array>
               <array dataType="xsd:integer" dictRef="t:prim" size="2">25 92</array>
               <array dataType="xsd:integer" dictRef="t:cont" size="2">15 45</array>
               <array dataType="xsd:string" dictRef="t:basis" size="2">DZP def2-TZVP</array>
               <array dataType="xsd:string" dictRef="t:contraction" size="2">[4s2p1dI8s4p1d] [6s4p4d1fI17s11p7d1f]</array>
            </list>
        </module>
    </comment>
```
