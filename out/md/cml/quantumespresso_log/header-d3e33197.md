# header {#header-d3e33197}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | QuantumEspresso log                                                                                                                                                                                   |
| id                                                                                                                                                                                                    | header                                                                                                                                                                                                |
| name                                                                                                                                                                                                  | Program version                                                                                                                                                                                       |
| pattern                                                                                                                                                                                               | \^\\s\*Program\\s\*.\*starts\\son.\*                                                                                                                                                                  |
| endPattern                                                                                                                                                                                            | .\*                                                                                                                                                                                                   |
| endOffset                                                                                                                                                                                             | 0                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | ./initialization/header.xml                                                                                                                                                                           |

######Template attributes

**Input.**

     Program PWSCF v.6.1 (svn rev. 13369) starts on 28Sep2017 at 18:37:43 
        

**Output text.**

```xml
<comment class="example.output" id="header">
        <module cmlx:templateRef="header">
             <scalar dataType="xsd:string" dictRef="cc:program">QuantumEspresso</scalar>
             <scalar dataType="xsd:string" dictRef="cc:module">PWSCF</scalar>
             <scalar dataType="xsd:string" dictRef="cc:programVersion">6.1</scalar>
             <scalar dataType="xsd:string" dictRef="cc:programSubversion">13369</scalar>
             <scalar dataType="xsd:date" dictRef="cc:rundate">2017-09-28T18:37:43.000+02:00</scalar>
        </module> 
    </comment>
```
