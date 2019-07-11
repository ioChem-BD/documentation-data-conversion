# mulliken {#mulliken-d3e9187}

Gaussian log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Gaussian log                                                                                                                                        |
| id                                                                                                                                                  | mulliken                                                                                                                                            |
| name                                                                                                                                                | mulliken                                                                                                                                            |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| newline                                                                                                                                             | \$                                                                                                                                                  |
| pattern                                                                                                                                             | \\s\*Mulliken\\s\*(\[Aa\]tomic)?\\s\*charges:\\s\*                                                                                                  |
| endPattern                                                                                                                                          | \\s\*Charge=.\*                                                                                                                                     |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | l601.mulliken.xml                                                                                                                                   |

######Template attributes

**Input.**

     Mulliken atomic charges:
                  1
         1  C   -0.619218
         2  H    0.154804
         3  H    0.154804
         4  H    0.154804
         5  H    0.154804
     Sum of Mulliken charges=   0.00000
     Atomic charges with hydrogens summed into heavy atoms:
                  1
         1  C    0.000000
         2  H    0.000000
         3  H    0.000000
         4  H    0.000000
         5  H    0.000000
     Sum of Mulliken charges=   0.00000
     Electronic spatial extent (au):  <R**2>=    36.2154
     Charge=     0.0000 electrons
      

**Output text.**

```xml
<comment class="example.output" id="l601.mulliken">
    <module cmlx:templateRef="mulliken">
      <module cmlx:lineCount="8" cmlx:templateRef="l601.mullik">
        <scalar dataType="xsd:string" dictRef="g:title">Mulliken atomic charges:</scalar>
        <scalar dataType="xsd:integer" dictRef="cc:serial">1</scalar>
        <list cmlx:lineCount="5" cmlx:templateRef="row">
          <array dataType="xsd:integer" dictRef="cc:serial" size="5">1 2 3 4 5</array>
          <array dataType="xsd:string" dictRef="cc:elementType" size="5">C H H H H</array>
          <array dataType="xsd:double" dictRef="x:charge" size="5">-0.619218 0.154804 0.154804 0.154804 0.154804</array>
        </list>
        <scalar dataType="xsd:string" dictRef="x:type">Mulliken</scalar>
        <scalar dataType="xsd:double" dictRef="x:chargesum">0.0</scalar>
      </module>
      <module cmlx:lineCount="8" cmlx:templateRef="l601.mullik">
        <scalar dataType="xsd:string" dictRef="g:title">Atomic charges with hydrogens summed into heavy atoms:</scalar>
        <scalar dataType="xsd:integer" dictRef="cc:serial">1</scalar>
        <list cmlx:lineCount="5" cmlx:templateRef="row">
          <array dataType="xsd:integer" dictRef="cc:serial" size="5">1 2 3 4 5</array>
          <array dataType="xsd:string" dictRef="cc:elementType" size="5">C H H H H</array>
          <array dataType="xsd:double" dictRef="x:charge" size="5">0.0 0.0 0.0 0.0 0.0</array>
        </list>
        <scalar dataType="xsd:string" dictRef="x:type">Mulliken</scalar>
        <scalar dataType="xsd:double" dictRef="x:chargesum">0.0</scalar>
      </module>
      <scalar dataType="xsd:double" dictRef="g:electextent2">36.2154</scalar>
      <scalar dataType="xsd:double" dictRef="g:charge">0.0</scalar>
    </module>
  </comment>
```

-   [l601.mullikenspin](/out/md/cml/gaussian_log/l601.mullikenspin-d3e9226.md)
