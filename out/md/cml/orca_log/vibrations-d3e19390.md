# vibrations {#vibrations-d3e19390}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | vibrations                                                                                                                                          |
| name                                                                                                                                                | Vibrational frequencies                                                                                                                             |
| pattern                                                                                                                                             | \\s\*\\-+\\s\*\$\\s\*VIBRATIONAL\\sFREQUENCIES.\*                                                                                                   |
| endPattern                                                                                                                                          | \\s\*\\-+\\s\*\$(?!(NORMALIVIBRATIONAL)).\*\$\\s\*\\-+\\s\*                                                                                         |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | vibrations.xml                                                                                                                                      |

######Template attributes

**Input.**

    -----------------------
    VIBRATIONAL FREQUENCIES
    -----------------------

       0:         0.00 cm**-1
       1:         0.00 cm**-1
       2:         0.00 cm**-1
       3:         0.00 cm**-1
       4:         0.00 cm**-1
       5:         0.00 cm**-1
       6:      -434.84 cm**-1 ***imaginary mode***
       7:      -419.45 cm**-1 ***imaginary mode***
       8:      -289.83 cm**-1 ***imaginary mode***
       9:      -272.32 cm**-1 ***imaginary mode***
      10:      -168.02 cm**-1 ***imaginary mode***
      11:      -122.97 cm**-1 ***imaginary mode***
      12:      -114.81 cm**-1 ***imaginary mode***
      13:      -110.33 cm**-1 ***imaginary mode***
      14:       -68.54 cm**-1 ***imaginary mode***
      15:       -51.59 cm**-1 ***imaginary mode***
      16:       -30.16 cm**-1
      17:        12.43 cm**-1
      18:        48.29 cm**-1
      19:        56.20 cm**-1
      20:        76.33 cm**-1
    ...
     119:      3560.03 cm**-1
     120:      3687.73 cm**-1
     121:      3905.08 cm**-1
     122:      3910.12 cm**-1


    ------------
    NORMAL MODES
    ------------

    These modes are the cartesian displacements weighted by the diagonal matrix
    M(i,i)=1/sqrt(m[i]) where m[i] is the mass of the displaced atom
    Thus, these vectors are normalized but *not* orthogonal

                      0          1          2          3          4          5
          0       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
          1       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
          2       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
          3       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
          4       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
          5       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
          6       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
          7       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
          8       0.000000   0.000000   0.000000   0.000000   0.000000   0.000000
    ...
        120       0.158785   0.002231  -0.004623
        121      -0.160155  -0.002115   0.004968
        122      -0.035114  -0.000336   0.001664

        

**Output text.**

```xml
<comment class="example.output" id="vibrations">
      <module cmlx:templateRef="vibrations">
         <array dataType="xsd:double" dictRef="cc:frequency" size="123">0.00 0.00 0.00 0.00 0.00 0.00 -434.84 -419.45 -289.83 -272.32 -168.02 -122.97 -114.81 -110.33 -68.54 -51.59 -30.16 12.43 48.29 56.20 76.33 ... 3560.03 3687.73 3905.08 3910.12</array>
         <matrix cols="123" dataType="xsd:double" dictRef="cc:displacement" rows="123">0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 ... -0.000121 -0.000040 -0.000235 -0.000016 0.000051 0.000049 -0.000072 0.000062 0.000277 0.000188 0.000023 -0.000067 0.000039 0.000005 -0.000052 0.000067 0.000027 0.000108 -0.000026 -0.000007 0.000011 0.000079 -0.000014 0.000017 0.000008 -0.000181 0.000019 0.000405 -0.000100 0.001416 -0.004623 0.004968 0.001664</matrix>
     </module>         
    </comment>
```
