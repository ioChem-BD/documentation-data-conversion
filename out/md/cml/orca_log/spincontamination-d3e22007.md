# spincontamination {#spincontamination-d3e22007}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | spincontamination                                                                                                                                   |
| name                                                                                                                                                | UHF Spin contamination                                                                                                                              |
| pattern                                                                                                                                             | \\s\*-{10,}\\s\*\$\\s\*UHF\\sSPIN\\sCONTAMINATION\\s\*                                                                                              |
| endPattern                                                                                                                                          | \\s\*-{10,}\$\\s\*\\w                                                                                                                               |
| endPattern2                                                                                                                                         | \\s+\\\*{20,}.\*                                                                                                                                    |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | scf/spincontamination.xml                                                                                                                           |

######Template attributes

**Input.**

    ----------------------
    UHF SPIN CONTAMINATION
    ----------------------

    Warning: in a DFT calculation there is little theoretical justification to 
             calculate <S**2> as in Hartree-Fock theory. We will do it anyways
             but you should keep in mind that the values have only limited relevance

    Expectation value of <S**2>     :     2.002400
    Ideal value S*(S+1) for S=1.0   :     2.000000
    Deviation                       :     0.002400

    ----------------        
        

**Output text.**

```xml
<comment class="example.output" id="spincontamination">
        <module cmlx:templateRef="spincontamination" dictRef="cc:userDefinedModule">
           <scalar dataType="xsd:double" dictRef="cc:s2">2.002400</scalar>
           <scalar dataType="xsd:double" dictRef="cc:sideal">1.0</scalar>
           <scalar dataType="xsd:double" dictRef="cc:s2ideal">2.000000</scalar>
           <scalar dataType="xsd:double" dictRef="cc:s2deviation">0.002400</scalar>
        </module>
    </comment>
```
