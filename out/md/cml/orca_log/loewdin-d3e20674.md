# loewdin {#loewdin-d3e20674}

Orca log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Orca log                                                                                                                                                                                              |
| id                                                                                                                                                                                                    | loewdin                                                                                                                                                                                               |
| name                                                                                                                                                                                                  | Loewdin atomic charges                                                                                                                                                                                |
| pattern                                                                                                                                                                                               | \\s\*-{10,}\\s\*\$\\s\*LOEWDIN\\sATOMIC\\sCHARGES\\s\*                                                                                                                                                |
| endPattern                                                                                                                                                                                            | ((?!-{10,}).)\*\$\\s\*                                                                                                                                                                                |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | loewdin.xml                                                                                                                                                                                           |

######Template attributes

**Input.**

    ----------------------
    LOEWDIN ATOMIC CHARGES
    ----------------------
       0 O :   -0.168228
       1 O :   -0.179552
       2 H :    0.085567
       3 H :    0.034534
       4 H :    0.027223
       5 H :    0.081890
       6 O :   -0.309948
       7 C :    0.075544
       8 C :   -0.069700
       9 C :   -0.070619
      10 H :    0.000462
      11 H :    0.028464
      12 H :    0.023274
      13 H :    0.027059
      14 H :    0.030993
      15 H :    0.012906
      16 O :   -0.263879
      17 N :    0.065363
      18 N :    0.035438
      19 C :   -0.055862
      20 C :   -0.081573
      21 C :    0.086648
      22 C :    0.043026
      23 C :   -0.038364
      24 C :   -0.022781
      25 C :    0.010833
      26 C :    0.022212
      27 H :    0.033425
      28 H :    0.039272
      29 H :    0.031010
      30 H :    0.032703
      31 H :    0.045044
      32 H :    0.040696
      33 H :    0.018023
      34 H :    0.033863
      35 H :    0.043084
      36 H :    0.038351
      37 H :    0.035667
      38 H :    0.054584
      39 H :    0.077998
      40 H :    0.045348
        
        

**Output text.**

```xml
<comment class="example.output" id="loewdin">
      <module cmlx:templateRef="loewdin">
         <module cmlx:templateRef="loewdin">
            <array dataType="xsd:integer" dictRef="cc:serial" size="41">0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40</array>
            <array dataType="xsd:string" dictRef="cc:elementType" size="41">O O H H H H O C C C H H H H H H O N N C C C C C C C C H H H H H H H H H H H H H H</array>
            <array dataType="xsd:double" dictRef="x:charge" size="41">-0.168228 -0.179552 0.085567 0.034534 0.027223 0.081890 -0.309948 0.075544 -0.069700 -0.070619 0.000462 0.028464 0.023274 0.027059 0.030993 0.012906 -0.263879 0.065363 0.035438 -0.055862 -0.081573 0.086648 0.043026 -0.038364 -0.022781 0.010833 0.022212 0.033425 0.039272 0.031010 0.032703 0.045044 0.040696 0.018023 0.033863 0.043084 0.038351 0.035667 0.054584 0.077998 0.045348</array>
         </module>
      </module>   
    </comment>
```