# unrestrictedorbitals {#unrestrictedorbitals-d3e34195}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole control file                                                                                                                              |
| id                                                                                                                                                  | unrestrictedorbitals                                                                                                                                |
| name                                                                                                                                                | Unrestricted orbitals sections                                                                                                                      |
| pattern                                                                                                                                             | \\s\*\\u0024(alphaIbeta)\\sshells.\*                                                                                                                |
| endPattern                                                                                                                                          | \\s\*\\u0024.\*                                                                                                                                     |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | orbitals/unrestricted.xml                                                                                                                           |

######Template attributes

**Input.**

     $alpha shells
     a1      1-57                                   ( 1 )
     a2      1-32                                   ( 1 )
     e       1-84                                   ( 1 )
     $beta shells   
        

**Input.**

     $beta shells
     a1      1-57                                   ( 1 )
     a2      1-32                                   ( 1 )
     e       1-84                                   ( 1 )
     $scfiterlimit       50     
        

**Output text.**

```xml
<comment class="example.output" id="unrestrictedorbitals">
     <module cmlx:templateRef="unrestrictedorbitals">
         <scalar dataType="xsd:string" dictRef="t:spintype">alpha</scalar>
         <array dataType="xsd:string" dictRef="t:label" size="3">a1 a2 e</array>
         <array dataType="xsd:string" dictRef="t:mosrange" size="3">1-57 1-32 1-84</array>
      </module>
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="unrestrictedorbitals2">   
      <module cmlx:templateRef="unrestrictedorbitals">
         <scalar dataType="xsd:string" dictRef="t:spintype">beta</scalar>
         <array dataType="xsd:string" dictRef="t:label" size="3">a1 a2 e</array>
         <array dataType="xsd:string" dictRef="t:mosrange" size="3">1-57 1-32 1-84</array>
      </module>   
    </comment>
```
