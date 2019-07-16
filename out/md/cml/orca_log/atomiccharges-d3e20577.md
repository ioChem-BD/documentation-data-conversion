# atomiccharges {#atomiccharges-d3e20577}

Orca log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Orca log                                                                                                                                                                                              |
| id                                                                                                                                                                                                    | atomiccharges                                                                                                                                                                                         |
| name                                                                                                                                                                                                  | Mulliken Atomic Population Analysis                                                                                                                                                                   |
| pattern                                                                                                                                                                                               | \\s\*-{10,}\\s\*\$\\s\*MULLIKEN\\sATOMIC\\sCHARGES\\s\*                                                                                                                                               |
| endPattern                                                                                                                                                                                            | ((?!-{10,}).)\*\$\\s\*                                                                                                                                                                                |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | atomiccharges.xml                                                                                                                                                                                     |

######Template attributes

**Input.**

    -----------------------
    MULLIKEN ATOMIC CHARGES
    -----------------------
       0 O :   -0.352546
       1 O :   -0.338177
       2 H :    0.181202
       3 H :    0.153731
       4 H :    0.156442
       5 H :    0.173788
       6 O :   -0.438569
       7 C :    0.096672
       8 C :   -0.007270
       9 C :   -0.049441
      10 H :    0.007249
      11 H :    0.012378
      12 H :    0.015108
      13 H :    0.028145
      14 H :    0.034518
      15 H :   -0.001598
      16 O :   -0.281057
      17 N :   -0.219891
      18 N :   -0.038276
      19 C :    0.017713
      20 C :   -0.148609
      21 C :    0.090160
      22 C :    0.132917
      23 C :   -0.041825
      24 C :    0.011202
      25 C :    0.005651
      26 C :    0.004627
      27 H :    0.043101
      28 H :    0.047589
      29 H :    0.030649
      30 H :    0.031734
      31 H :    0.066707
      32 H :    0.058984
      33 H :    0.011669
      34 H :    0.039520
      35 H :    0.050871
      36 H :    0.045359
      37 H :    0.040962
      38 H :    0.074987
      39 H :    0.137087
      40 H :    0.116541
    Sum of atomic charges:   -0.0000000 

        

**Output text.**

```xml
<comment class="example.output" id="atomiccharges">
        <module cmlx:templateRef="atomiccharges">
            <scalar dataType="xsd:double" dictRef="x:chargesum">-0.0000000</scalar>
            <array dataType="xsd:integer" dictRef="cc:serial" size="41">0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40</array>
            <array dataType="xsd:string" dictRef="cc:elementType" size="41">O O H H H H O C C C H H H H H H O N N C C C C C C C C H H H H H H H H H H H H H H</array>
            <array dataType="xsd:double" dictRef="x:charge" size="41">-0.352546 -0.338177 0.181202 0.153731 0.156442 0.173788 -0.438569 0.096672 -0.007270 -0.049441 0.007249 0.012378 0.015108 0.028145 0.034518 -0.001598 -0.281057 -0.219891 -0.038276 0.017713 -0.148609 0.090160 0.132917 -0.041825 0.011202 0.005651 0.004627 0.043101 0.047589 0.030649 0.031734 0.066707 0.058984 0.011669 0.039520 0.050871 0.045359 0.040962 0.074987 0.137087 0.116541</array>
         </module>
    </comment>
```