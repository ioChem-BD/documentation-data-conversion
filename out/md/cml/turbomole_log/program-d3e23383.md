# program {#program-d3e23383}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Turbomole log                                                                                                                                                                                         |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| id                                                                                                                                                                                                    | program                                                                                                                                                                                               |
| name                                                                                                                                                                                                  | Program version and runtime                                                                                                                                                                           |
| pattern                                                                                                                                                                                               | \\s\*\\w\*\\s\*\\(.\*\\)\\s\*\\:\\s\*TURBOMOLE.\*                                                                                                                                                     |
| endPattern                                                                                                                                                                                            | \\s\*Copyright.\*                                                                                                                                                                                     |
| endOffset                                                                                                                                                                                             | 4                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | program.version.xml                                                                                                                                                                                   |

######Template attributes

**Input.**

     statpt(maginet-iv108) : TURBOMOLE V6.3 7 Feb 2011 at 15:58:30
     Copyright (C) 2011 TURBOMOLE GmbH, Karlsruhe
     
     
     2011-12-15 08:13:20.786 
      

**Input.**

     relax(maginet-ii146) : TURBOMOLE V5-8-0 24 Nov 2005 at 22:47:17
     Copyright (C) 2005 University of Karlsruhe


        2010-12-23 03:10:52.701
      

**Output text.**

```xml
<comment class="example.output" id="program2">
 ridft (maginet165) : TURBOMOLE V6.6( 19134 ) 3 Jun 2014 at 14:53:30
 Copyright (C) 2014 TURBOMOLE GmbH, Karlsruhe


    2015-02-13 10:10:20.395  
  </comment>
```

**Output text.**

```xml
<comment class="example.output" id="program">
      <module cmlx:templateRef="program">   
           <list cmlx:templateRef="prog">
                <scalar dataType="xsd:string" dictRef="t:module">statpt</scalar>
                <scalar dataType="xsd:string" dictRef="cc:hostname">maginet-iv108</scalar>
                <scalar dataType="xsd:string" dictRef="cc:program">TURBOMOLE</scalar>
                <scalar dataType="xsd:string" dictRef="cc:programDate">7 Feb 2011 at 15:58:30</scalar>
                <scalar dataType="xsd:string" dictRef="cc:programVersion" id="programVersion">6.3</scalar>      
           </list>
           <scalar dataType="xsd:date" dictRef="cc:date">2011-12-15T08:13:20Z</scalar>         
      </module>         
  </comment>
```

**Output text.**

```xml
<comment class="example.output" id="program3">
    <module cmlx:templateRef="program">
        <list cmlx:templateRef="prog">
           <scalar dataType="xsd:string" dictRef="t:module">relax</scalar>
           <scalar dataType="xsd:string" dictRef="cc:hostname">maginet-ii146</scalar>
           <scalar dataType="xsd:string" dictRef="cc:program">TURBOMOLE</scalar>
           <scalar dataType="xsd:string" dictRef="cc:programVersion">5-8-0</scalar>
           <scalar dataType="xsd:string" dictRef="cc:programDate">24 Nov 2005 at 22:47:17</scalar>
        </list>
        <scalar dataType="xsd:date" dictRef="cc:date">2010-12-23T03:10:52.701+01:00</scalar>
     </module>
  </comment>
```
