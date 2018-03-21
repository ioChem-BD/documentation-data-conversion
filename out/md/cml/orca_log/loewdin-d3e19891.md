# loewdin {#loewdin-d3e19891}

Orca log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | loewdin                                                                                                                                             |
| name                                                                                                                                                | Loewdin atomic charges and spin populations                                                                                                         |
| pattern                                                                                                                                             | \\s\*-{10,}\\s\*\$\\s\*LOEWDIN\\sATOMIC\\sCHARGES\\sAND\\sSPIN\\s(POPULATIONSIDENSITIES)\\s\*                                                       |
| endPattern                                                                                                                                          | ((?!-{10,}).)\*\$\\s\*                                                                                                                              |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | loewdinspin.xml                                                                                                                                     |

######Template attributes

**Input.**

    -------------------------------------------
    LOEWDIN ATOMIC CHARGES AND SPIN POPULATIONS
    -------------------------------------------
       0 Cu:    0.492244    0.690963
       1 Cu:    0.492244    0.690964
       2 N :   -0.164072    0.071495
       3 N :   -0.164072    0.071495
       4 N :   -0.164071    0.071495
       5 N :   -0.164071    0.071495
       6 N :    0.006321    0.013273
       7 N :    0.006321    0.013273
       8 N :   -0.094685    0.073185
       9 N :   -0.094685    0.073185
      10 N :   -0.094685    0.073185
      11 N :   -0.094685    0.073185
      12 N :   -0.176858   -0.001194
      13 N :   -0.176858   -0.001194
      14 H :    0.113526    0.001952
      15 H :    0.113526    0.001952
      16 H :    0.113526    0.001952
      17 H :    0.113526    0.001952
      18 H :    0.128906    0.001342
      19 H :    0.128906    0.001342
      20 H :    0.128906    0.001342
      21 H :    0.128906    0.001342
      22 H :    0.168521    0.000725
      23 H :    0.168521    0.000725
      24 H :    0.168521    0.000725
      25 H :    0.168521    0.000725
      26 H :    0.119923   -0.000126
      27 H :    0.119923   -0.000126
      28 H :    0.126988   -0.000158
      29 H :    0.126988   -0.000158
      30 H :    0.126988   -0.000158
      31 H :    0.126988   -0.000158

        

**Output text.**

```xml
<comment class="example.output" id="loewdin">
        <module cmlx:templateRef="loewdin">
           <array dataType="xsd:integer" dictRef="cc:serial" size="32">0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31</array>
           <array dataType="xsd:string" dictRef="cc:elementType" size="32">Cu Cu N N N N N N N N N N N N H H H H H H H H H H H H H H H H H H</array>
           <array dataType="xsd:double" dictRef="x:charge" size="32">0.492244 0.492244 -0.164072 -0.164072 -0.164071 -0.164071 0.006321 0.006321 -0.094685 -0.094685 -0.094685 -0.094685 -0.176858 -0.176858 0.113526 0.113526 0.113526 0.113526 0.128906 0.128906 0.128906 0.128906 0.168521 0.168521 0.168521 0.168521 0.119923 0.119923 0.126988 0.126988 0.126988 0.126988</array>
           <array dataType="xsd:double" dictRef="x:spin" size="32">0.690963 0.690964 0.071495 0.071495 0.071495 0.071495 0.013273 0.013273 0.073185 0.073185 0.073185 0.073185 -0.001194 -0.001194 0.001952 0.001952 0.001952 0.001952 0.001342 0.001342 0.001342 0.001342 0.000725 0.000725 0.000725 0.000725 -0.000126 -0.000126 -0.000158 -0.000158 -0.000158 -0.000158</array>
        </module>
    </comment>
```