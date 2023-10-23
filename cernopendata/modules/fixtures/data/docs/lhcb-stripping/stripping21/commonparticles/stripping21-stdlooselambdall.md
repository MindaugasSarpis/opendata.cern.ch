[\[stripping21 lines\]](../stripping21-index.md)

# StdLooseLambdaLL

**CombineParticles/StdLooseLambdaLL**

|                  |                                                                                                                                                                              |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdLoosePions](../commonparticles/stripping21-stdloosepions.md)/Particles', 'Phys/[StdLooseProtons](../commonparticles/stripping21-stdlooseprotons.md)/Particles'\] |
| DaughtersCuts    | {'p+': '(P\>2\*GeV) & (MIPCHI2DV(PRIMARY)\>9)', 'pi+': '(P\>2\*GeV) & (MIPCHI2DV(PRIMARY)\>9)'}                                                                              |
| CombinationCut   | (ADAMASS('Lambda0')\<50\*MeV) & (ADOCACHI2CUT(30, ''))                                                                                                                       |
| MotherCut        | (ADMASS('Lambda0')\<35\*MeV) & (VFASPF(VCHI2)\<30)                                                                                                                           |
| DecayDescriptor  | \[Lambda0 -\> p+ pi-\]cc                                                                                                                                                     |
| DecayDescriptors | \[\]                                                                                                                                                                         |
| Output           | None                                                                                                                                                                         |
