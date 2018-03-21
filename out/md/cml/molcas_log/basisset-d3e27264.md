# basisset {#basisset-d3e27264}


| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/Total.png)                                                                                                                                |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | MOLCAS log                                                                                                                                          |
| id                                                                                                                                                  | basisset                                                                                                                                            |
| name                                                                                                                                                | Basis set section                                                                                                                                   |
| pattern                                                                                                                                             | \\s\*Basis\\sset\\slabel.\*                                                                                                                         |
| endPattern                                                                                                                                          | \\s\*\\\*{10,}.\*                                                                                                                                   |
| endPattern2                                                                                                                                         | \~                                                                                                                                                  |
| endPattern3                                                                                                                                         | \\-\\-.\*                                                                                                                                           |
| endPattern4                                                                                                                                         | \\+\\+\\s\*Molecular\\sstructure\\sinfo.\*                                                                                                          |
| endOffset                                                                                                                                           | 0                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | modules/basisset.xml                                                                                                                                |

######Template attributes

**Input.**

          Basis set label:C.CC-PVTZ.......... 

          Valence basis set:
          ==================
          Associated Effective Charge  6.000000 au
          Associated Actual Charge     6.000000 au
          Nuclear Model: Point charge


          Shell  nPrim  nBasis  Cartesian Spherical Contaminant
             s      10       4        X                  
             p       5       3        X                  
             d       2       2                 X         
             f       1       1                 X         
          Basis set label:O.CC-PVTZ......... 

          Valence basis set:
          ==================
          Associated Effective Charge  8.000000 au
          Associated Actual Charge     8.000000 au
          Nuclear Model: Point charge


          Shell  nPrim  nBasis  Cartesian Spherical Contaminant
             s      10       4        X                  
             p       5       3        X                  
             d       2       2                 X         
             f       1       1                 X         
          Basis set label:H.CC-PVTZ......... 

          Valence basis set:
          ==================
          Associated Effective Charge  1.000000 au
          Associated Actual Charge     1.000000 au
          Nuclear Model: Point charge


          Shell  nPrim  nBasis  Cartesian Spherical Contaminant
             s       5       3        X                  
             p       2       2        X                  
             d       1       1                 X         


    ++       Molecular structure info:

        

**Input.**

          Basis set label:C.ANO-S...3S2P. 
     
          Valence basis set:
          ------------------
          Associated Effective Charge  6.000000 au
          Associated Actual Charge     6.000000 au
          Nuclear Model: Point charge
     
          Shell  nPrim  nBasis  Cartesian Spherical Contaminant
             s      10       3        X                  
             p       6       2        X                  
     
     
          Basis set label:O.ANO-S...3S2P. 
     
          Valence basis set:
          ------------------
          Associated Effective Charge  8.000000 au
          Associated Actual Charge     8.000000 au
          Nuclear Model: Point charge
     
          Shell  nPrim  nBasis  Cartesian Spherical Contaminant
             s      10       3        X                  
             p       6       2        X                  
     
     
          Basis set label:H.ANO-S...2S. 
     
          Valence basis set:
          ------------------
          Associated Effective Charge  1.000000 au
          Associated Actual Charge     1.000000 au
          Nuclear Model: Point charge
     
          Shell  nPrim  nBasis  Cartesian Spherical Contaminant
             s       7       2        X                  
    --
     
     
    ++    Molecular structure info: 
        

**Output text.**

```xml
<comment class="example.output" id="basisset">
         <module cmlx:templateRef="basisset">
            <module cmlx:templateRef="section">
               <array dataType="xsd:string" delimiter="I" dictRef="m:basis" size="12">CICC-PVTZIIIIIIIIII</array>
               <module cmlx:templateRef="valence">
                  <scalar dataType="xsd:double" dictRef="m:effectivecharge">6.000000</scalar>
                  <scalar dataType="xsd:double" dictRef="m:actualCharge">6.000000</scalar>
                  <list cmlx:templateRef="shells">
                     <array dataType="xsd:string" dictRef="m:shell" size="4">s p d f</array>
                     <array dataType="xsd:integer" dictRef="m:nprim" size="4">10 5 2 1</array>
                     <array dataType="xsd:integer" dictRef="m:nbasis" size="4">4 3 2 1</array>
                  </list>
               </module>
            </module>
            <module cmlx:templateRef="section">
               <array dataType="xsd:string" delimiter="I" dictRef="m:basis" size="11">OICC-PVTZIIIIIIIII</array>
               <module cmlx:templateRef="valence">
                  <scalar dataType="xsd:double" dictRef="m:effectivecharge">8.000000</scalar>
                  <scalar dataType="xsd:double" dictRef="m:actualCharge">8.000000</scalar>
                  <list cmlx:templateRef="shells">
                     <array dataType="xsd:string" dictRef="m:shell" size="4">s p d f</array>
                     <array dataType="xsd:integer" dictRef="m:nprim" size="4">10 5 2 1</array>
                     <array dataType="xsd:integer" dictRef="m:nbasis" size="4">4 3 2 1</array>
                  </list>
               </module>
            </module>
            <module cmlx:templateRef="section">
               <array dataType="xsd:string" delimiter="I" dictRef="m:basis" size="11">HICC-PVTZIIIIIIIII</array>
               <module cmlx:templateRef="valence">
                  <scalar dataType="xsd:double" dictRef="m:effectivecharge">1.000000</scalar>
                  <scalar dataType="xsd:double" dictRef="m:actualCharge">1.000000</scalar>
                  <list cmlx:templateRef="shells">
                     <array dataType="xsd:string" dictRef="m:shell" size="3">s p d</array>
                     <array dataType="xsd:integer" dictRef="m:nprim" size="3">5 2 1</array>
                     <array dataType="xsd:integer" dictRef="m:nbasis" size="3">3 2 1</array>
                  </list>
               </module>
            </module>
         </module>    
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="basisset2">
        <module cmlx:templateRef="basisset">
            <module cmlx:templateRef="section">
               <array dataType="xsd:string" delimiter="I" dictRef="m:basis" size="6">CIANO-SIII3S2PI</array>
               <module cmlx:templateRef="valence">
                  <scalar dataType="xsd:double" dictRef="m:effectivecharge">6.000000</scalar>
                  <scalar dataType="xsd:double" dictRef="m:actualCharge">6.000000</scalar>
                  <list cmlx:templateRef="shells">
                     <array dataType="xsd:string" dictRef="m:shell" size="2">s p</array>
                     <array dataType="xsd:integer" dictRef="m:nprim" size="2">10 6</array>
                     <array dataType="xsd:integer" dictRef="m:nbasis" size="2">3 2</array>
                  </list>
               </module>
            </module>
            <module cmlx:templateRef="section">
               <array dataType="xsd:string" delimiter="I" dictRef="m:basis" size="6">OIANO-SIII3S2PI</array>
               <module cmlx:templateRef="valence">
                  <scalar dataType="xsd:double" dictRef="m:effectivecharge">8.000000</scalar>
                  <scalar dataType="xsd:double" dictRef="m:actualCharge">8.000000</scalar>
                  <list cmlx:templateRef="shells">
                     <array dataType="xsd:string" dictRef="m:shell" size="2">s p</array>
                     <array dataType="xsd:integer" dictRef="m:nprim" size="2">10 6</array>
                     <array dataType="xsd:integer" dictRef="m:nbasis" size="2">3 2</array>
                  </list>
               </module>
            </module>
            <module cmlx:templateRef="section">
               <array dataType="xsd:string" delimiter="I" dictRef="m:basis" size="6">HIANO-SIII2SI</array>
               <module cmlx:templateRef="valence">
                  <scalar dataType="xsd:double" dictRef="m:effectivecharge">1.000000</scalar>
                  <scalar dataType="xsd:double" dictRef="m:actualCharge">1.000000</scalar>
                  <list cmlx:templateRef="shells">
                     <array dataType="xsd:string" dictRef="m:shell" size="1">s</array>
                     <array dataType="xsd:integer" dictRef="m:nprim" size="1">7</array>
                     <array dataType="xsd:integer" dictRef="m:nbasis" size="1">2</array>
                  </list>
               </module>
            </module>
         </module>    
    </comment>
```
