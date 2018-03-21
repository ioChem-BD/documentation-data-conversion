# parameters {#parameters-d3e34177}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole control file                                                                                                                              |
| id                                                                                                                                                  | parameters                                                                                                                                          |
| name                                                                                                                                                | Control parameters                                                                                                                                  |
| pattern                                                                                                                                             | \\s\*\\u0024(?i:(scfinstabIricc2IstatptIexopt)).\*                                                                                                  |
| pattern2                                                                                                                                            | \\s\*\\u0024(?i:(riIrijIrir12))\\s\*                                                                                                                |
| endPattern                                                                                                                                          | \\s\*\\u0024.\*                                                                                                                                     |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | parameters.xml                                                                                                                                      |

######Template attributes

**Input.**

    $scfinstab rpas     
        

**Input.**

    $rij
        

**Input.**

    $rir12
      ansatz      2
      ccsdapprox  ccsd(f12)
      no_f12metric
      r12model    B
      comaprox    F+K
      cabs        svd  1.0000E-08
      examp       fixed  noflip
      corrfac     LCG
      cabsingles  on    
        

**Input.**

    $ricc2
      mp2
      ccsd
      ccsd(t)   
        

**Output text.**

```xml
<comment class="example.output" id="parameters">
        <module cmlx:templateRef="parameters">
            <scalar dataType="xsd:string" dictRef="t:scfinstab">rpas</scalar>
        </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="parameters2">
        <module cmlx:templateRef="parameters">
            <scalar dataType="xsd:string" dictRef="t:rir12">rir12</scalar>
        </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="parameters3">
        <module cmlx:templateRef="parameters">
            <scalar dataType="xsd:string" dictRef="t:ri">rir12</scalar>
        </module> 
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="parameters4">
        <module cmlx:templateRef="parameters">
            <scalar dataType="xsd:string" dictRef="t:ricc2">ricc2</scalar>
        </module> 
    </comment>
```
