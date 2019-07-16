# restrictedorbitals {#restrictedorbitals-d3e36606}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole control file                                                                                                                                                                                |
| id                                                                                                                                                                                                    | restrictedorbitals                                                                                                                                                                                    |
| name                                                                                                                                                                                                  | Restricted orbitals sections                                                                                                                                                                          |
| pattern                                                                                                                                                                                               | \\s\*\\u0024closed\\sshell.\*                                                                                                                                                                         |
| endPattern                                                                                                                                                                                            | \\s\*\\u0024.\*                                                                                                                                                                                       |
| endPattern2                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | orbitals/restricted.xml                                                                                                                                                                               |

######Template attributes

**Input.**

     $closed shells
     a1      1-57                                   ( 2 )
     a2      1-32                                   ( 2 )
     e       1-84                                   ( 2 )
     $scfiterlimit       40     
        

**Output text.**

```xml
<comment class="example.output" id="restrictedorbitals">
       <module cmlx:templateRef="restrictedorbitals">
         <array dataType="xsd:string" dictRef="t:label" size="3">a1 a2 e</array>
         <array dataType="xsd:string" dictRef="t:mosrange" size="3">1-57 1-32 1-84</array>
      </module>
    </comment>
```
