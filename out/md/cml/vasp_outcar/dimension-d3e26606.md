# dimension {#dimension-d3e26606}

VASP outcar

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Partial.png)                                                                                                                              |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | dimension                                                                                                                                           |
| name                                                                                                                                                | Dimension of arrays section                                                                                                                         |
| pattern                                                                                                                                             | \\s\*Dimension\\sof\\sarrays:.\*                                                                                                                    |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| xml:base                                                                                                                                            | dimension.xml                                                                                                                                       |

######Template attributes

**Input.**

     Dimension of arrays:
       k-points           NKPTS =      5   k-points in BZ     NKDIM =      5   number of bands    NBANDS=    192
       number of dos      NEDOS =    301   number of ions     NIONS =     49
       non local maximal  LDIM  =      8   non local SUM 2l+1 LMDIM =     32
       total plane-waves  NPLWV = 290304
       max r-space proj   IRMAX =   3928   max aug-charges    IRDMAX=  12951
       dimension x,y,z NGX =    48 NGY =   48 NGZ =  126
       dimension x,y,z NGXF=    96 NGYF=   96 NGZF=  252
       support grid    NGXF=    96 NGYF=   96 NGZF=  252
       ions per type =              12  24   3  10

        

**Output text.**

```xml
<comment class="example.output" id="dimension">
        <module cmlx:templateRef="dimension">
            <module cmlx:templateRef="atomtypes">
                <list cmlx:templateRef="missingID">
                    <array dataType="xsd:integer" dictRef="cc:atomcount" size="4">12 24 3 10</array>
                </list>
            </module>
        </module> 
    </comment>
```
