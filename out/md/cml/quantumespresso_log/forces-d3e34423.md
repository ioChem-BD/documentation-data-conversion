# forces {#forces-d3e34423}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | QuantumEspresso log                                                                                                                                                                                   |
| id                                                                                                                                                                                                    | forces                                                                                                                                                                                                |
| name                                                                                                                                                                                                  | forces                                                                                                                                                                                                |
| pattern                                                                                                                                                                                               | \^\\s+Total\\s(Dispersion\\s)?\[Ff\]orce.\*                                                                                                                                                           |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | forces.xml                                                                                                                                                                                            |

######Template attributes

**Input.**

         Total force =     0.013129     Total SCF correction =     0.000094
        
        

**Input.**

         Total Dispersion Force =     0.067387
        
        

**Output text.**

```xml
<comment class="example.output" id="force">
        <module cmlx:templateRef="forces">        
            <scalar dataType="xsd:double" dictRef="cc:force" units="nonsi2:ev.angstrom-1">0.3375602847997187</scalar>
            <scalar dataType="xsd:double" dictRef="qex:scfCorrection" units="nonsi2:ev.angstrom-1">0.002416838050969119</scalar>                        
        </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="force2">
        <module cmlx:templateRef="forces">
            <scalar dataType="xsd:double" dictRef="qex:dispenergy" units="nonsi2:ev.angstrom-1">1.7325900610708087</scalar>
        </module>
    </comment>
```
