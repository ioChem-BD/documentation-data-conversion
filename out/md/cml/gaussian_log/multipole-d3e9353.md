# multipole {#multipole-d3e9353}

Gaussian log


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Gaussian log                                                                                                                                        |
| id                                                                                                                                                  | multipole                                                                                                                                           |
| name                                                                                                                                                | multipole                                                                                                                                           |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| pattern                                                                                                                                             | \\s\*Dipole moment.\*                                                                                                                               |
| endPattern                                                                                                                                          | (\\s\*N\\-N=.\*)                                                                                                                                    |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | l601.multipole.xml                                                                                                                                  |

######Template attributes

**Input.**

     Dipole moment (field-independent basis, Debye):
        X=     0.0000    Y=     0.0000    Z=     0.0000  Tot=     0.0000
     Quadrupole moment (field-independent basis, Debye-Ang):
       XX=    -8.3036   YY=    -8.3036   ZZ=    -8.3036
       XY=     0.0000   XZ=     0.0000   YZ=     0.0000
     Traceless Quadrupole moment (field-independent basis, Debye-Ang):
       XX=     0.0000   YY=     0.0000   ZZ=     0.0000
       XY=     0.0000   XZ=     0.0000   YZ=     0.0000
     Octapole moment (field-independent basis, Debye-Ang**2):
      XXX=     0.0000  YYY=     0.0000  ZZZ=     0.0000  XYY=     0.0000
      XXY=     0.0000  XXZ=     0.0000  XZZ=     0.0000  YZZ=     0.0000
      YYZ=     0.0000  XYZ=    -0.7195
     Hexadecapole moment (field-independent basis, Debye-Ang**3):
     XXXX=   -16.2252 YYYY=   -16.2252 ZZZZ=   -16.2252 XXXY=     0.0000
     XXXZ=     0.0000 YYYX=     0.0000 YYYZ=     0.0000 ZZZX=     0.0000
     ZZZY=     0.0000 XXYY=    -4.9297 XXZZ=    -4.9297 YYZZ=    -4.9297
     XXYZ=     0.0000 YYXZ=     0.0000 ZZXY=     0.0000
      N-N= 1.339525332293D+01 E-N=-1.198300348205D+02  KE= 4.007106437468D+01
      

**Output text.**

```xml
<comment class="example.output" id="l601.multipole">
    <module cmlx:templateRef="multipole">
      <array dataType="xsd:double" size="3" dictRef="cc:dipole">0.0 0.0 0.0</array>
      <scalar dataType="xsd:double" dictRef="x:dipole">0.0</scalar>
      <array dataType="xsd:double" size="3" dictRef="cc:quadrupole">-8.3036 -8.3036 -8.3036</array>
      <array dataType="xsd:double" size="3" dictRef="cc:quadrupole">0.0 0.0 0.0</array>
      <array dataType="xsd:double" size="6" dictRef="cc:quadrupole">0.0 0.0 0.0 0.0 0.0 0.0</array>
      <array dataType="xsd:double" size="10" dictRef="cc:octapole">0.0 0.0 0.0 0.0 0.0 0.0 0.0 0.0 0.0 -0.7195</array>
      <array dataType="xsd:double" size="15" dictRef="cc:hexadecapole">-16.2252 -16.2252 -16.2252 0.0 0.0 0.0 0.0 0.0 0.0 -4.9297 -4.9297 -4.9297 0.0 0.0 0.0</array>
    </module>
 </comment>
```
