# cosmo {#cosmo-d3e24713}

Turbomole log

| Type                                                                                                                                                | Status                                                                                                                                              |
|----|----|
| CML extraction template                                                                                                                             | ![](/imgs/Total.png)                                                                                                                                |
| HTML5 representation                                                                                                                                | ![](/imgs/None.png)                                                                                                                                 |

######Implementation level

| Attribute                                                                                                                                           | Value                                                                                                                                               |
|----|----|
| *source*                                                                                                                                            | Turbomole log                                                                                                                                       |
| id                                                                                                                                                  | cosmo                                                                                                                                               |
| name                                                                                                                                                | Cosmo results                                                                                                                                       |
| pattern                                                                                                                                             | \\s\*----|\\s\*\$\\s\*COSMO\\sRESULTS\\s\*\$\\s\*----|\\s\*                                                                                               |
| endPattern                                                                                                                                          | \\s\*----|\\s\*\$\\s\*                                                                                                                                 |
| endOffset                                                                                                                                           | 1                                                                                                                                                   |
| repeat                                                                                                                                              | \*                                                                                                                                                  |
| xml:base                                                                                                                                            | cosmo.xml                                                                                                                                           |

######Template attributes

**Input.**

     ============================================================================== 
                                      COSMO RESULTS
     ============================================================================== 
      PARAMETER:
        nppa:      1082
        nspa:        92
        nsph:        32
        nps:        712
        npspher:    224
        disex:   10.0000    
        disex2:  4128.15    
        rsolv [A]: 3.5400
        routf:     0.8500
        phsran:   0.00    
        ampran:   0.10E-04
        cavity:  closed
        epsilon:  9.800
        fepsi:      0.8543689
      CAVITY VOLUME/AREA [a.u.]:
        surface: V1.0, A matrix: V1.0
        area:   654.69
        volume:  1389.84
      SCREENING CHARGE:
        cosmo      :  -0.024349
        correction :   0.024631
        total      :   0.000282
      ENERGIES [a.u.]:
        Total energy            =    -1650.4710944278
        Total energy + OC corr. =    -1650.4709392488
        Dielectric energy       =       -0.0050408508
        Diel. energy + OC corr. =       -0.0048856718
        The following value is included for downward compatibility
        Total energy corrected  =    -1650.4710168383
      RADII [Angstroem]:
        atom       1     2     3     4     5     6     7     8     9    10    11  
        radius  2.00  2.00  2.00  2.00  2.00  1.06  2.00  2.00  2.00  2.00  2.00 
        atom      12    13    14    15    16    17    18    19    20    21  
        radius  1.30  1.30  1.30  1.30  1.30  1.30  1.30  1.30  1.30  1.30 
     ==============================================================================     
        

**Input.**

**Output text.**

```xml
<comment class="example.output" id="cosmo">
       <module cmlx:lineCount="39" cmlx:templateRef="cosmo">
          <list cmlx:templateRef="parameters">
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">nppa</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">1082</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">nspa</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">92</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">nsph</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">32</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">nps</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">712</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">npspher</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">224</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">disex</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">10.0000</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">disex2</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">4128.15</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">rsolv [A]</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">3.5400</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">routf</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.8500</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">phsran</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.00</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">ampran</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.10E-04</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">cavity</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">closed</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">epsilon</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">9.800</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">fepsi</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.8543689</scalar>
              </list>
          </list>
          <list cmlx:templateRef="cavityVolumeArea">
              <list>
                  <scalar dataType="xsd:string" dictRef="t:surface">V1.0</scalar>
                  <scalar dataType="xsd:string" dictRef="t:matrix">V1.0</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">area</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">654.69</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">volume</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">1389.84</scalar>
              </list>
          </list>
          <list cmlx:templateRef="screeningCharge">
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">cosmo</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">-0.024349</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">correction</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.024631</scalar>
              </list>
              <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">total</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.000282</scalar>
              </list>
          </list>
          <list id="energies" cmlx:templateRef="energies">
              <scalar dataType="xsd:double" dictRef="cc:energy">-1650.4710944278</scalar>
              <scalar dataType="xsd:double" dictRef="t:energyOcCorr">-1650.4709392488</scalar>
              <scalar dataType="xsd:double" dictRef="t:dielectricEnergy">-0.0050408508</scalar>
              <scalar dataType="xsd:double" dictRef="t:dielectricEnergyOcCorr">-0.0048856718</scalar>
              <scalar dataType="xsd:double" dictRef="t:energyCorrected">-1650.4710168383</scalar>
          </list>
          <list id="radii" cmlx:templateRef="radii">
              <array dataType="xsd:integer" size="21" dictRef="cc:serial">1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21</array>
              <array dataType="xsd:double" size="21" dictRef="t:radius">2.0 2.0 2.0 2.0 2.0 1.06 2.0 2.0 2.0 2.0 2.0 1.3 1.3 1.3 1.3 1.3 1.3 1.3 1.3 1.3 1.3</array>
          </list>
      </module>   
    </comment>
```

**Output text.**

```xml
<comment class="example.output" id="cosmo2">
        <module cmlx:templateRef="cosmo">
            <list cmlx:templateRef="parameters">
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">nppa</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">1082</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">nspa</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">92</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">nsph</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">32</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">nps</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">351</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">npspher</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">197</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">disex</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">10.0000</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">disex2</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">4473.83</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">rsolv [A]</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">1.3000</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">routf</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.8500</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">phsran</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.0</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">ampran</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.10E-04</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">cavity</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">closed</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">epsilon</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">infinity</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">refind</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">1.300</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">fepsi</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">1.0000000</scalar>
               </list>
            </list>
            <list cmlx:templateRef="cavityVolumeArea">
               <list>
                  <scalar dataType="xsd:string" dictRef="t:surface">V1.0</scalar>
                  <scalar dataType="xsd:string" dictRef="t:matrix">V1.0</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">area</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">349.52</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">volume</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">542.84</scalar>
               </list>
            </list>
            <list cmlx:templateRef="screeningCharge">
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">cosmo</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">-0.019014</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">correction</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">0.018692</scalar>
               </list>
               <list>
                  <scalar dataType="xsd:string" dictRef="t:parameter">total</scalar>
                  <scalar dataType="xsd:string" dictRef="t:value">-0.000323</scalar>
               </list>
            </list>
            <list cmlx:templateRef="energies" id="energies">
               <scalar dataType="xsd:double" dictRef="cc:energy">-190.8500889093</scalar>
               <scalar dataType="xsd:double" dictRef="t:energyOcCorr">-190.8501078686</scalar>
               <scalar dataType="xsd:double" dictRef="t:dielectricEnergy">-0.0158822461</scalar>
               <scalar dataType="xsd:double" dictRef="t:dielectricEnergyOcCorr">-0.0159012054</scalar>
            </list>
            <list cmlx:templateRef="radii" id="radii">
               <array dataType="xsd:string" dictRef="cc:elementType" size="3">o c h</array>
               <array dataType="xsd:double" dictRef="t:atomicradii" size="3">1.72 2.00 1.30</array>
               <array dataType="xsd:string" dictRef="t:atomrange" size="3">1 2-4 5-8</array>
            </list>
         </module>
    </comment>
```
