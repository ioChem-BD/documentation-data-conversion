# basis {#basis-d3e20262}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Orca log                                                                                                                                            |
| id                                                                                                                                                  | basis                                                                                                                                               |
| name                                                                                                                                                | Basis Set Information                                                                                                                               |
| pattern                                                                                                                                             | \\s\*\\-+\\s\*\$\\s\*BASIS\\sSET\\sINFORMATION\\s\*\$\\s\*\\-+\\s\*                                                                                 |
| endPattern                                                                                                                                          | \\s+\\\*{5,}.\*                                                                                                                                     |
| endPattern2                                                                                                                                         | \\-+.\*\$\\S+.\*\$\\-+.\*                                                                                                                           |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| xml:base                                                                                                                                            | basis.xml                                                                                                                                           |

######Template attributes

**Input.**

    ---------------------
    BASIS SET INFORMATION
    ---------------------
    There are 4 groups of distinct atoms

     Group   1 Type O   : 7s4p1d contracted to 3s2p1d pattern {511/31/1}
     Group   2 Type H   : 4s1p contracted to 2s1p pattern {31/1}
     Group   3 Type C   : 7s4p1d contracted to 3s2p1d pattern {511/31/1}
     Group   4 Type N   : 7s4p1d contracted to 3s2p1d pattern {511/31/1}

    Atom   0O    basis set group =>   1
    Atom   1O    basis set group =>   1
    Atom   2H    basis set group =>   2
    Atom   3H    basis set group =>   2
    Atom   4H    basis set group =>   2
    Atom   5H    basis set group =>   2
    Atom   6O    basis set group =>   1
    Atom   7C    basis set group =>   3
    Atom   8C    basis set group =>   3
    Atom   9C    basis set group =>   3
    Atom  10H    basis set group =>   2
    Atom  11H    basis set group =>   2
    Atom  12H    basis set group =>   2
    Atom  13H    basis set group =>   2
    Atom  14H    basis set group =>   2
    Atom  15H    basis set group =>   2
    Atom  16O    basis set group =>   1
    Atom  17N    basis set group =>   4
    Atom  18N    basis set group =>   4
    Atom  19C    basis set group =>   3
    Atom  20C    basis set group =>   3
    Atom  21C    basis set group =>   3
    Atom  22C    basis set group =>   3
    Atom  23C    basis set group =>   3
    Atom  24C    basis set group =>   3
    Atom  25C    basis set group =>   3
    Atom  26C    basis set group =>   3
    Atom  27H    basis set group =>   2
    Atom  28H    basis set group =>   2
    Atom  29H    basis set group =>   2
    Atom  30H    basis set group =>   2
    Atom  31H    basis set group =>   2
    Atom  32H    basis set group =>   2
    Atom  33H    basis set group =>   2
    Atom  34H    basis set group =>   2
    Atom  35H    basis set group =>   2
    Atom  36H    basis set group =>   2
    Atom  37H    basis set group =>   2
    Atom  38H    basis set group =>   2
    Atom  39H    basis set group =>   2
    Atom  40H    basis set group =>   2
    -------------------------------
        

**Output text.**

```xml
<comment class="example.output" id="basis">
      <module cmlx:templateRef="basis">        
         <list cmlx:templateRef="group">
            <array dataType="xsd:integer" dictRef="o:group" size="4">1 2 3 4</array>
            <array dataType="xsd:string" dictRef="o:primitive" size="4">7s4p1d 4s1p 7s4p1d 7s4p1d</array>
            <array dataType="xsd:string" dictRef="o:contraction" size="4">3s2p1d 2s1p 3s2p1d 3s2p1d</array>
         </list>
         <list dictRef="atombasis">
            <array dataType="xsd:integer" dictRef="cc:serial" size="41">0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40</array>
            <array dataType="xsd:string" dictRef="cc:elementType" size="41">O O H H H H O C C C H H H H H H O N N C C C C C C C C H H H H H H H H H H H H H H</array>
            <array dataType="xsd:integer" dictRef="o:group" size="41">1 1 2 2 2 2 1 3 3 3 2 2 2 2 2 2 1 4 4 3 3 3 3 3 3 3 3 2 2 2 2 2 2 2 2 2 2 2 2 2 2</array>
         </list>
      </module>
    </comment>
```
