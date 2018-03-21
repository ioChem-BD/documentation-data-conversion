# finalspenergy {#finalspenergy-d3e20402}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | finalspenergy                                                                                                                                       |
| name                                                                                                                                                | Final Single Point Energy                                                                                                                           |
| pattern                                                                                                                                             | \\s\*-{20,}.\*\$\\s\*FINAL\\sSINGLE\\sPOINT\\sENERGY.\*                                                                                             |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | energies/final.xml                                                                                                                                  |

######Template attributes

**Input.**

    -------------------------   ----------------
    FINAL SINGLE POINT ENERGY    -3947.384041263
    -------------------------   ----------------

        

**Input.**

    -------------------------   --------------------
    FINAL SINGLE POINT ENERGY     -1339.461219357614   (SCF not fully converged!)
    -------------------------   --------------------
        

**Output text.**

```xml
<comment class="example.output" id="finalspenergy">
      <module cmlx:templateRef="finalspenergy">
         <scalar dataType="xsd:double" dictRef="cc:energy">-3947.384041263</scalar>
      </module>       
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="finalspenergy2">
      <module cmlx:templateRef="finalspenergy">
         <scalar dataType="xsd:double" dictRef="cc:energy">-1339.461219357614</scalar>
      </module>
    </comment>
```
