# input.file {#input.file-d3e5763}


| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/Total.png)                                                                                                                                                                                  |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | ADF log                                                                                                                                                                                               |
| id                                                                                                                                                                                                    | input.file                                                                                                                                                                                            |
| name                                                                                                                                                                                                  | Input file dump                                                                                                                                                                                       |
| pattern                                                                                                                                                                                               | \\s\*\\(INPUT\\sFILE\\)\\s\*                                                                                                                                                                          |
| endPattern                                                                                                                                                                                            | \\s\*(End InputIend inputIEND INPUTIEnd input)\\s\*                                                                                                                                                   |
| endPattern2                                                                                                                                                                                           | \\s\*\$\\s\*\\\*{40,}+\\s\*                                                                                                                                                                           |
| endPattern3                                                                                                                                                                                           | \~                                                                                                                                                                                                    |
| endOffset                                                                                                                                                                                             | 1                                                                                                                                                                                                     |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| xml:base                                                                                                                                                                                              | input.file.xml                                                                                                                                                                                        |

######Template attributes

**Input.**

    (INPUT FILE)

    create W /usr/local/adf2007.01/atomicdata/ZORA/TZP/W.4d
    xc
    lda vwn
    gradients becke perdew
    end
    relativistic scalar zora
    corepotentials t12rel <++
    W 2
    end
    end input

        

**Output text.**

```xml
<comment class="example.output" id="input.file">
      <module cmlx:lineCount="13" cmlx:templateRef="input.file">    
        <scalar dataType="xsd:string" dictRef="cc:inputLine">(INPUT FILE)</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine" />
        <scalar dataType="xsd:string" dictRef="cc:inputLine">create W /usr/local/adf2007.01/atomicdata/ZORA/TZP/W.4d</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine">xc</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine">lda vwn</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine">gradients becke perdew</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine">end</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine">relativistic scalar zora</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine">corepotentials t12rel <++</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine">W 2</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine">end</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine">end input</scalar>
        <scalar dataType="xsd:string" dictRef="cc:inputLine" />
      </module>   
    </comment>
```
