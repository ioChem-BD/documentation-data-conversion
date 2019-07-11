# process.info {#process.info-d3e5710}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | ADF log                                                                                                                                             |
| id                                                                                                                                                  | process.info                                                                                                                                        |
| name                                                                                                                                                | Parallel Execution: Process Information                                                                                                             |
| pattern                                                                                                                                             | \\s\*Parallel\\sExecution:\\sProcess\\sInformation.\*                                                                                               |
| endPattern                                                                                                                                          | \\s\*\\(INPUT\\sFILE\\)\\s\*                                                                                                                        |
| endPattern2                                                                                                                                         | \\s\*\\\*{20,}+\\s+                                                                                                                                 |
| endPattern3                                                                                                                                         | \~                                                                                                                                                  |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | process.info.xml                                                                                                                                    |

######Template attributes

**Input.**

     Parallel Execution: Process Information
     =======================================

     Actual Number of Tasks running:    4
     The Master (kid 0) runs on host maginet-ii190

      Kid Node                   Speed          Task ID   Status
    ------------------------------------------------------------------
        0 maginet-ii190             -1                0
        1 maginet-ii190             -1                1
        2 maginet-ii190             -1                2
        3 maginet-ii190             -1                3
     
     Communication Options:
     ----------------------
     Broadcast:            4
     Gather   :            4
     Combine  :            4    
        

**Input.**

     Parallel Execution: Process Information
     ==============================================================================
     Rank   Node Name                              NodeID   MyNodeRank  NodeMaster
        0   maginet-ii205                             0          0          0
        1   maginet-ii205                             0          1         -1
        2   maginet-ii205                             0          2         -1
        3   maginet-ii205                             0          3         -1
        4   maginet-ii205                             0          4         -1
        5   maginet-ii205                             0          5         -1
        6   maginet-ii205                             0          6         -1
        7   maginet-ii205                             0          7         -1
        8   maginet-ii210                             1          0          1
        9   maginet-ii210                             1          1         -1
       10   maginet-ii210                             1          2         -1
       11   maginet-ii210                             1          3         -1
       12   maginet-ii210                             1          4         -1
       13   maginet-ii210                             1          5         -1
       14   maginet-ii210                             1          6         -1
       15   maginet-ii210                             1          7         -1
     ==============================================================================
        

**Output text.**

```xml
<comment class="example.output" id="process.info">      
    <module cmlx:lineCount="63" cmlx:templateRef="process.info"> 
          <array dataType="xsd:string" size="4" dictRef="cc:nodeName">maginet-ii190 maginet-ii190 maginet-ii190 maginet-ii190</array> 
      </module>        
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="process.info2">     
    <module cmlx:lineCount="63" cmlx:templateRef="process.info"> 
      <array dataType="xsd:string" size="16" dictRef="cc:nodeName">maginet-ii205 maginet-ii205 maginet-ii205 maginet-ii205 maginet-ii205 maginet-ii205 maginet-ii205 maginet-ii205 maginet-ii210 maginet-ii210 maginet-ii210 maginet-ii210 maginet-ii210 maginet-ii210 maginet-ii210 maginet-ii210</array> 
    </module>      
  </comment>
```
