# bonds {#bonds-d3e20802}

Orca log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Orca log                                                                                                                                                                                              |
| id                                                                                                                                                                                                    | bonds                                                                                                                                                                                                 |
| name                                                                                                                                                                                                  | Mayer bond orders larger than 0.1                                                                                                                                                                     |
| pattern                                                                                                                                                                                               | \\s\*Mayer\\sbond\\sorders\\slarger\\sthan\\s.\*                                                                                                                                                      |
| endPattern                                                                                                                                                                                            | \\s\*                                                                                                                                                                                                 |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | bonds.xml                                                                                                                                                                                             |

######Template attributes

**Input.**

      Mayer bond orders larger than 0.1
    B(  0-O ,  2-H ) :   0.9898 B(  0-O ,  3-H ) :   0.9071 B(  1-O ,  4-H ) :   0.8801 
    B(  1-O ,  5-H ) :   0.9839 B(  1-O , 33-H ) :   0.1848 B(  3-H ,  6-O ) :   0.1409 
    B(  4-H ,  6-O ) :   0.1800 B(  6-O ,  7-C ) :   1.3907 B(  6-O , 40-H ) :   0.1566 
    B(  7-C ,  8-C ) :   1.0247 B(  7-C , 10-H ) :   0.8911 B(  7-C , 20-C ) :   0.5980 
    B(  8-C ,  9-C ) :   1.1090 B(  8-C , 11-H ) :   0.9202 B(  8-C , 12-H ) :   0.9273 
    B(  9-C , 13-H ) :   0.9649 B(  9-C , 14-H ) :   0.9589 B(  9-C , 15-H ) :   0.9474 
    B( 16-O , 18-N ) :   0.1147 B( 16-O , 26-C ) :   2.0236 B( 17-N , 21-C ) :   1.4568 
    B( 17-N , 22-C ) :   0.9096 B( 17-N , 25-C ) :   0.9178 B( 18-N , 26-C ) :   1.3955 
    B( 18-N , 39-H ) :   0.9143 B( 18-N , 40-H ) :   0.8496 B( 19-C , 20-C ) :   1.0614 
    B( 19-C , 27-H ) :   0.9549 B( 19-C , 28-H ) :   0.9496 B( 19-C , 29-H ) :   0.9517 
    B( 20-C , 21-C ) :   1.2532 B( 20-C , 30-H ) :   0.9059 B( 21-C , 31-H ) :   0.9486 
    B( 22-C , 23-C ) :   1.0878 B( 22-C , 32-H ) :   0.9320 B( 22-C , 33-H ) :   0.8878 
    B( 23-C , 24-C ) :   1.0882 B( 23-C , 34-H ) :   0.9322 B( 23-C , 35-H ) :   0.9356 
    B( 24-C , 25-C ) :   1.0522 B( 24-C , 36-H ) :   0.9353 B( 24-C , 37-H ) :   0.9328 
    B( 25-C , 26-C ) :   0.8818 B( 25-C , 38-H ) :   0.8971
        

**Output text.**

```xml
<comment class="example.output" id="bonds">   
        <module cmlx:templateRef="bonds">
            <array dataType="xsd:double" dictRef="x:distance" size="44">0.9898 0.9071 0.8801 0.9839 0.1848 0.1409 0.1800 1.3907 0.1566 1.0247 0.8911 0.5980 1.1090 0.9202 0.9273 0.9649 0.9589 0.9474 0.1147 2.0236 1.4568 0.9096 0.9178 1.3955 0.9143 0.8496 1.0614 0.9549 0.9496 0.9517 1.2532 0.9059 0.9486 1.0878 0.9320 0.8878 1.0882 0.9322 0.9356 1.0522 0.9353 0.9328 0.8818 0.8971</array>
            <matrix cols="2" dataType="xsd:integer" dictRef="x:serial" rows="44">0 2 0 3 1 4 1 5 1 33 3 6 4 6 6 7 6 40 7 8 7 10 7 20 8 9 8 11 8 12 9 13 9 14 9 15 16 18 16 26 17 21 17 22 17 25 18 26 18 39 18 40 19 20 19 27 19 28 19 29 20 21 20 30 21 31 22 23 22 32 22 33 23 24 23 34 23 35 24 25 24 36 24 37 25 26 25 38</matrix>
         </module>
    </comment>
```
