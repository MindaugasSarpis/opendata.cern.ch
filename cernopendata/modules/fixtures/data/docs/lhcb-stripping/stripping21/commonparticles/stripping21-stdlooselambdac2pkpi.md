[\[stripping21 lines\]](../stripping21-index.md)

# StdLooseLambdac2PKPi

**CombineParticles/StdLooseLambdac2PKPi**

|                  |                                                                                                                                                                                                                                                                 |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdLooseKaons](../commonparticles/stripping21-stdloosekaons.md)/Particles', 'Phys/[StdLoosePions](../commonparticles/stripping21-stdloosepions.md)/Particles', 'Phys/[StdLooseProtons](../commonparticles/stripping21-stdlooseprotons.md)/Particles'\] |
| DaughtersCuts    | {'K+': '(P \> 2\*GeV)', 'p+': '(P \> 2\*GeV)', 'pi+': '(P \> 2\*GeV)'}                                                                                                                                                                                          |
| CombinationCut   | ((ADAMASS('Lambda_c+')\<110\*MeV) & (APT\>1.\*GeV) & (ADOCAMAX('')\<0.5\*mm))                                                                                                                                                                                   |
| MotherCut        | ((VFASPF(VCHI2) \< 30) & (ADMASS('Lambda_c+')\<100\*MeV) & (BPVVDCHI2\>36) & (BPVDIRA\>0.98))                                                                                                                                                                   |
| DecayDescriptor  | \[Lambda_c+ -\> K- p+ pi+\]cc                                                                                                                                                                                                                                   |
| DecayDescriptors | \[\]                                                                                                                                                                                                                                                            |
| Output           | None                                                                                                                                                                                                                                                            |
