[\[stripping21 lines\]](../stripping21-index.md)

# StrippingWeAKTJetsLine

## Properties:

|                |                              |
|----------------|------------------------------|
| OutputLocation | Phys/WeAKTJetsLine/Particles |
| Postscale      | 1.0000000                    |
| HLT            | None                         |
| Prescale       | 1.0000000                    |
| L0DU           | None                         |
| ODIN           | None                         |

## Filter sequence:

CheckPV/checkPVmin0

|        |     |
|--------|-----|
| MinPVs | 0   |
| MaxPVs | -1  |

LoKi::VoidFilter/SelFilterPhys_StdAllNoPIDsElectrons_Particles

|      |                                                                                                                |
|------|----------------------------------------------------------------------------------------------------------------|
| Code | CONTAINS('Phys/[StdAllNoPIDsElectrons](../commonparticles/stripping21-stdallnopidselectrons.md)/Particles')\>0 |

FilterDesktop/selWeAKTJetsWe

|                 |                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------|
| Code            |                                                                                               |
| Inputs          | \[ 'Phys/[StdAllNoPIDsElectrons](../commonparticles/stripping21-stdallnopidselectrons.md)' \] |
| DecayDescriptor | None                                                                                          |
| Output          | Phys/selWeAKTJetsWe/Particles                                                                 |

LoKi::VoidFilter/SelFilterPhys_StdJets_Particles

|      |                                                                                    |
|------|------------------------------------------------------------------------------------|
| Code | CONTAINS('Phys/[StdJets](../commonparticles/stripping21-stdjets.md)/Particles')\>0 |

CombineParticles/WeAKTJetsLine

|                  |                                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| Inputs           | \[ 'Phys/[StdJets](../commonparticles/stripping21-stdjets.md)' , 'Phys/selWeAKTJetsWe' \] |
| DaughtersCuts    | { '' : 'ALL' , 'CELLjet' : ' (PT \> 15.0 \* GeV ) ' , 'e+' : 'ALL' , 'e-' : 'ALL' }       |
| CombinationCut   | AALLSAMEBPV & ( dr_13 \> 0.5 )& ( dr_23 \> 0.5 )                                          |
| MotherCut        | ALL                                                                                       |
| DecayDescriptor  | \[H+ -\> CELLjet CELLjet e+\]cc                                                           |
| DecayDescriptors | \[ '\[H+ -\> CELLjet CELLjet e+\]cc' \]                                                   |
| Output           | Phys/WeAKTJetsLine/Particles                                                              |
