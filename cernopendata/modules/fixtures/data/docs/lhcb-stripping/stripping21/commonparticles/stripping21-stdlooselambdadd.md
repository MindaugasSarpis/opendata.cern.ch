[\[stripping21 lines\]](../stripping21-index.md)

# StdLooseLambdaDD

**CombineParticles/StdLooseLambdaDD**

|                  |                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdNoPIDsDownPions](../commonparticles/stripping21-stdnopidsdownpions.md)/Particles', 'Phys/[StdNoPIDsDownProtons](../commonparticles/stripping21-stdnopidsdownprotons.md)/Particles'\] |
| DaughtersCuts    | {'p+': '(P\>2\*GeV) & (MIPCHI2DV(PRIMARY)\>4)', 'pi+': '(P\>2\*GeV) & (MIPCHI2DV(PRIMARY)\>4)'}                                                                                                  |
| CombinationCut   | (ADAMASS('Lambda0')\<80\*MeV) & (ADOCACHI2CUT(25, ''))                                                                                                                                           |
| MotherCut        | (ADMASS('Lambda0')\<64\*MeV) & (VFASPF(VCHI2)\<25)                                                                                                                                               |
| DecayDescriptor  | \[Lambda0 -\> p+ pi-\]cc                                                                                                                                                                         |
| DecayDescriptors | \[\]                                                                                                                                                                                             |
| Output           | None                                                                                                                                                                                             |
