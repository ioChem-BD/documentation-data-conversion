# l914\_excitations {#l914_excitations-d3e16004}

Gaussian log

| Type                                                                                                                                                                                                  | Status                                                                                                                                                                                                |
|----|----|
| CML extraction template                                                                                                                                                                               | ![](/imgs/Total.png)                                                                                                                                                                                  |
| HTML5 representation                                                                                                                                                                                  | ![](/imgs/None.png)                                                                                                                                                                                   |

######Implementation level

| Attribute                                                                                                                                                                                             | Value                                                                                                                                                                                                 |
|----|----|
| *source*                                                                                                                                                                                              | Gaussian log                                                                                                                                                                                          |
| id                                                                                                                                                                                                    | l914\_excitations                                                                                                                                                                                     |
| name                                                                                                                                                                                                  | Time-dependent DFT excitations                                                                                                                                                                        |
| repeat                                                                                                                                                                                                | \*                                                                                                                                                                                                    |
| pattern                                                                                                                                                                                               | \\s\*Excitation energies and oscillator strengths:\\s\*                                                                                                                                               |
| endPattern                                                                                                                                                                                            | \\s\*SavETr.\*                                                                                                                                                                                        |
| endOffset                                                                                                                                                                                             | 2                                                                                                                                                                                                     |
| xml:base                                                                                                                                                                                              | l914/l914\_excitations.xml                                                                                                                                                                            |

######Template attributes

**Input.**


     Excited State   1:      Singlet-A      3.3467 eV  370.46 nm  f=0.5317  <S**2>=0.000
          75 -> 76         0.69790
     This state for optimization and/or second-order correction.
     Total Energy, E(TD-HF/TD-KS) =  -974.346712524    
     Copying the excited state density for this state as the 1-particle RhoCI density.
     
     Excited State   2:      Singlet-A      3.8907 eV  318.67 nm  f=0.0065  <S**2>=0.000
          74 -> 76         0.66892
          75 -> 77         0.20436
     
     Excited State   3:      Singlet-A      4.2803 eV  289.66 nm  f=0.0019  <S**2>=0.000
          72 -> 76        -0.25494
          73 -> 76         0.63171
          75 -> 77        -0.13245
    SavETr:  write IOETrn=   770 NScale= 10 NData=  16 NLR=1 LETran=      64.
      

**Output text.**

```xml
<comment class="example.output" id="l914_excitations">
<module cmlx:templateRef="l914_excitations">
  <module cmlx:lineCount="6" cmlx:templateRef="l914_excitations1">
    <list cmlx:templateRef="l914_excit1">
      <list>
        <scalar dataType="xsd:integer" dictRef="g:tddft_enumber">1</scalar>
        <scalar dataType="xsd:string" dictRef="g:tddft_ttype">Singlet-A</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_eenergy">3.3467</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_wavelength">370.46</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_oscillator_strength">0.5317</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_s2">0.0</scalar>
      </list>
    </list>
    <list cmlx:templateRef="l914_excit2">
      <list>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalstart">75</scalar>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalend">76</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_unknown">0.6979</scalar>
      </list>
    </list>
    <list cmlx:templateRef="l914_tote">
      <scalar dataType="xsd:double" dictRef="g:tddft_totale">-974.346712524</scalar>
    </list>
  </module>
  <module cmlx:lineCount="4" cmlx:templateRef="l914_excitations1">
    <list cmlx:templateRef="l914_excit1">
      <list>
        <scalar dataType="xsd:integer" dictRef="g:tddft_enumber">2</scalar>
        <scalar dataType="xsd:string" dictRef="g:tddft_ttype">Singlet-A</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_eenergy">3.8907</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_wavelength">318.67</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_oscillator_strength">0.0065</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_s2">0.0</scalar>
      </list>
    </list>
    <list cmlx:templateRef="l914_excit2">
      <list>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalstart">74</scalar>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalend">76</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_unknown">0.66892</scalar>
      </list>
      <list>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalstart">75</scalar>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalend">77</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_unknown">0.20436</scalar>
      </list>
    </list>
  </module>
  <module cmlx:lineCount="5" cmlx:templateRef="l914_excitations1">
    <list cmlx:templateRef="l914_excit1">
      <list>
        <scalar dataType="xsd:integer" dictRef="g:tddft_enumber">3</scalar>
        <scalar dataType="xsd:string" dictRef="g:tddft_ttype">Singlet-A</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_eenergy">4.2803</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_wavelength">289.66</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_oscillator_strength">0.0019</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_s2">0.0</scalar>
      </list>
    </list>
    <list cmlx:templateRef="l914_excit2">
      <list>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalstart">72</scalar>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalend">76</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_unknown">-0.25494</scalar>
      </list>
      <list>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalstart">73</scalar>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalend">76</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_unknown">0.63171</scalar>
      </list>
      <list>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalstart">75</scalar>
        <scalar dataType="xsd:integer" dictRef="g:tddft_orbitalend">77</scalar>
        <scalar dataType="xsd:double" dictRef="g:tddft_unknown">-0.13245</scalar>
      </list>
    </list>
  </module>
</module>
</comment>
```
