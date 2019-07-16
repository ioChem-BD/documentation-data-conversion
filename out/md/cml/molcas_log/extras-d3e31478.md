# extras {#extras-d3e31478}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | MOLCAS log                                                                                                                                                                                            |
| id                                                                                                                                                                                                    | extras                                                                                                                                                                                                |
| name                                                                                                                                                                                                  | Extra lines                                                                                                                                                                                           |
| pattern                                                                                                                                                                                               | \\s\*Type\\sof\\s+Fock\\soperator\\sto\\suse.\*                                                                                                                                                       |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | modules/extras.xml                                                                                                                                                                                    |

######Template attributes

**Input.**

          Type of  Fock operator to use: STANDARD
          Type of HZERO operator to use: NON-STANDARD IPEA
          Extra imaginary denominator shift SHIFTI=      0.30000000
          Non-standard "IP-EA" denominator shift IPEAshift=      0.00000000
          The CANONICAL keyword was not used in the RASSCF program.
          Therefore, input orbitals should be transformed.
          The input orbitals and the CI vector will be transformed.

**Input.**

     
          Type of  Fock operator to use: STANDARD
          Type of HZERO operator to use: STANDARD IPEA
          Extra denominator shift SHIFT=      0.05000000
          The CANONICAL keyword was not used in the RASSCF program.
          Therefore, input orbitals should be transformed.
          The input orbitals and the CI vector will be transformed.

**Output text.**

```xml
<comment class="example.output" id="extras">
        <module cmlx:templateRef="extras">
            <scalar dataType="xsd:string" dictRef="m:fockoperator">STANDARD</scalar>
            <scalar dataType="xsd:string" dictRef="m:hzerooperator">NON-STANDARD IPEA</scalar>
            <scalar dataType="xsd:double" dictRef="m:shifti">0.30000000</scalar>
            <scalar dataType="xsd:double" dictRef="m:ipeashift">0.00000000</scalar>
        </module>        
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="extras2">
        <module cmlx:templateRef="extras">
            <scalar dataType="xsd:string" dictRef="m:fockoperator">STANDARD</scalar>
            <scalar dataType="xsd:string" dictRef="m:hzerooperator">STANDARD IPEA</scalar>
            <scalar dataType="xsd:double" dictRef="m:shift">0.05000000</scalar>
        </module>
    </comment>
```
