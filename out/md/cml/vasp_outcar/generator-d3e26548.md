# generator {#generator-d3e26548}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | VASP outcar                                                                                                                                         |
| id                                                                                                                                                  | generator                                                                                                                                           |
| name                                                                                                                                                | Program version                                                                                                                                     |
| pattern                                                                                                                                             | \\s\*vasp\\.\\d.\*                                                                                                                                  |
| endPattern                                                                                                                                          | \\s\*executed\\son.\*                                                                                                                               |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| xml:base                                                                                                                                            | generator.xml                                                                                                                                       |

######Template attributes

**Input.**

     vasp.5.3.2 13Sep12 (build Apr  2 2013 11:33:10) complex

     executed on             LinuxIFC date 2014.03.06  12:09:30
        

**Output text.**

```xml
<comment class="example.output" id="generator">
        <module cmlx:templateRef="generator">
            <scalar dataType="xsd:string" dictRef="cc:program">vasp</scalar>
            <scalar dataType="xsd:string" dictRef="cc:subversion">13Sep12 (build Apr  2 2013 11:33:10) complex</scalar>
            <scalar dataType="xsd:string" dictRef="v:platform">LinuxIFC</scalar>
            <scalar dataType="xsd:date" dictRef="cc:rundate">2014-03-06T12:09:30.000+01:00</scalar>
            <scalar dataType="xsd:string" dictRef="cc:programVersion">5.3.2</scalar>
        </module> 
    </comment>
```
