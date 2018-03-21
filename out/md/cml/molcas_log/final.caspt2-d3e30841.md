# final.caspt2 {#final.caspt2-d3e30841}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | final.caspt2                                                                                                                                        |
| name                                                                                                                                                | Final CASPT2 result                                                                                                                                 |
| pattern                                                                                                                                             | \\s\*FINAL\\sCASPT2\\sRESULT:.\*                                                                                                                    |
| endPattern                                                                                                                                          | \\+\\+\\sDenominators                                                                                                                               |
| endPattern2                                                                                                                                         | \\s{0,4}\\S.\*                                                                                                                                      |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/caspt2/final.caspt2.xml                                                                                                                     |

######Template attributes

**Input.**

      FINAL CASPT2 RESULT:

          Reference energy:        -190.6773098467
          E2 (Non-variational):      -0.6061449426
          Shift correction:          -0.0021160684
          E2 (Variational):          -0.6082610111
          Total energy:            -191.2855708577
          Residual norm:              0.0000004726
          Reference weight:           0.82136

          Contributions to the CASPT2 correlation energy
          Active & Virtual Only:         -0.1862740836
          One Inactive Excited:          -0.2303322543
          Two Inactive Excited:          -0.1895386047

**Output text.**

```xml
<comment class="example.output" id="final.caspt2">
        <module cmlx:templateRef="final.caspt2">
           <scalar dataType="xsd:double" dictRef="m:referener">-190.6773098467</scalar>
           <scalar dataType="xsd:double" dictRef="m:nonvare2">-0.6061449426</scalar>
           <scalar dataType="xsd:double" dictRef="m:shiftcorr">-0.0021160684</scalar>
           <scalar dataType="xsd:double" dictRef="m:vare2">-0.6082610111</scalar>
           <scalar dataType="xsd:double" dictRef="m:totalenergy">-191.2855708577</scalar>
           <scalar dataType="xsd:double" dictRef="m:residualnorm">0.0000004726</scalar>
           <scalar dataType="xsd:double" dictRef="m:refweight">0.82136</scalar>
           <scalar dataType="xsd:double" dictRef="m:activevirt">-0.1862740836</scalar>
           <scalar dataType="xsd:double" dictRef="m:oneeinactive">-0.2303322543</scalar>
           <scalar dataType="xsd:double" dictRef="m:twoinactive">-0.1895386047</scalar>
        </module>
    </comment>
```
