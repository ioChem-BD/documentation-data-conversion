# ci.expansion {#ci.expansion-d3e29424}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | ci.expansion                                                                                                                                        |
| name                                                                                                                                                | CI expansion specifications                                                                                                                         |
| pattern                                                                                                                                             | .\*CI\\sexpansion\\sspecifications.\*                                                                                                               |
| endPattern                                                                                                                                          | .\*\[0-9\]\$\\s\*(\\-\\-)?\\s\*                                                                                                                     |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/ci/ci.expansion.xml                                                                                                                         |

######Template attributes

**Input.**

         CI expansion specifications:
          ----------------------------
     
          Number of configuration state fnc.        10
          Number of determinants                    10
          Number of root(s) required                 7
          Root chosen for geometry opt.              7
          CI roots used                              1     2     3     4     5     6     7
          weights                                0.143 0.143 0.143 0.143 0.143 0.143 0.143
          highest root included in the CI            7
          max. size of the explicit Hamiltonian     10
     

**Input.**

          CI expansion specifications:
          ----------------------------

          Number of configuration state fnc.      1764
          Number of determinants                  2485
          Number of root(s) required                 1
          CI root used                               1
          highest root included in the CI            1
          Root passed to geometry opt.               1

**Output text.**

```xml
<comment class="example.output" id="ci.expansion">
    <module cmlx:templateRef="ci.expansion">
        <scalar dataType="xsd:integer" dictRef="m:conffnc">10</scalar>
        <scalar dataType="xsd:integer" dictRef="m:determinants">10</scalar>
        <scalar dataType="xsd:integer" dictRef="m:requiredroot">7</scalar>
        <scalar dataType="xsd:integer" dictRef="m:chosenroot">7</scalar>
        <array dataType="xsd:integer" dictRef="m:ciroots" size="7">1 2 3 4 5 6 7</array>
        <array dataType="xsd:double" dictRef="m:rootweight" size="7">0.143 0.143 0.143 0.143 0.143 0.143 0.143</array>
        <scalar dataType="xsd:integer" dictRef="m:highestroot">7</scalar>
        <scalar dataType="xsd:integer" dictRef="m:maxsizehamilt">10</scalar>
     </module>
  </comment>
```

**Output text.**

```xml
<comment class="example.output" id="ci.expansion2">     
      <module cmlx:templateRef="ci.expansion">
         <scalar dataType="xsd:integer" dictRef="m:conffnc">1764</scalar>
         <scalar dataType="xsd:integer" dictRef="m:determinants">2485</scalar>
         <scalar dataType="xsd:integer" dictRef="m:requiredroot">1</scalar>
         <array dataType="xsd:integer" dictRef="m:ciroots" size="1">1</array>
         <scalar dataType="xsd:integer" dictRef="m:highestroot">1</scalar>
         <scalar dataType="xsd:integer" dictRef="m:passedroot">1</scalar>
      </module>
  </comment>
```
