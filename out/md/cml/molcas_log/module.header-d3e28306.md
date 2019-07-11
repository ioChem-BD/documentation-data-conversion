# module.header {#module.header-d3e28306}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | module.header                                                                                                                                       |
| name                                                                                                                                                | Module header                                                                                                                                       |
| pattern                                                                                                                                             | \\s\*(\\(\\)){20,}\\s\*\$\\s\*MOLCAS\\sexecuting\\smodule.\*                                                                                        |
| pattern2                                                                                                                                            | \\s\*\-\--\\s\*Start\\s\*Module.\*                                                                                                                  |
| endPattern                                                                                                                                          | \\s\*                                                                                                                                               |
| endPattern2                                                                                                                                         | \\s\*\-\--\\s\*                                                                                                                                     |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/module.header.xml                                                                                                                           |

######Template attributes

**Input.**

    ()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()
                                      MOLCAS executing module SEWARD with 400 MB of memory                                  
                                                  at 14:02:49 Mon May 30 2011                                               
    ()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()

        

**Input.**

    --- Start Module: slapaf at Wed Jan 20 21:04:10 2016
        

**Output text.**

```xml
<comment class="example.output" id="module.header">
        <module cmlx:templateRef="module.header">
            <scalar dataType="xsd:string" dictRef="m:module">SEWARD</scalar>
            <scalar dataType="xsd:string" dictRef="cc:runDate">14:02:49 Mon May 30 2011</scalar>
        </module> 
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="">
        <module cmlx:templateRef="module.header">
            <scalar dataType="xsd:string" dictRef="m:module">slapaf</scalar>
            <scalar dataType="xsd:string" dictRef="cc:runDate">Wed Jan 20 21:04:10 2016</scalar>
        </module>
    </comment>
```
