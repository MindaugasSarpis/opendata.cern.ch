[\[stripping21 lines\]](../stripping21-index.md)

# StdLooseDetachedPhi2KK

**CombineParticles/StdLooseDetachedPhi2KK**

|                  |                                                                                       |
|------------------|---------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdLooseKaons](../commonparticles/stripping21-stdloosekaons.md)/Particles'\] |
| DaughtersCuts    | {'K+': '(MIPCHI2DV(PRIMARY) \> 4.)'}                                                  |
| CombinationCut   | (AM \< 1100.\*MeV) & (ADOCACHI2CUT(30,''))                                            |
| MotherCut        | (VFASPF(VCHI2) \< 25.0)                                                               |
| DecayDescriptor  | phi(1020) -\> K+ K-                                                                   |
| DecayDescriptors | \[\]                                                                                  |
| Output           | None                                                                                  |
