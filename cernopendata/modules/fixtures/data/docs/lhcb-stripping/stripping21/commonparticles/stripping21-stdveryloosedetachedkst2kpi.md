[\[stripping21 lines\]](../stripping21-index.md)

# StdVeryLooseDetachedKst2Kpi

**CombineParticles/StdVeryLooseDetachedKst2Kpi**

|                  |                                                                                                                                                                          |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdLooseKaons](../commonparticles/stripping21-stdloosekaons.md)/Particles', 'Phys/[StdLoosePions](../commonparticles/stripping21-stdloosepions.md)/Particles'\] |
| DaughtersCuts    | {}                                                                                                                                                                       |
| CombinationCut   | (ADAMASS('K\*(892)0')\<300\*MeV) & (ADOCACHI2CUT(30, ''))                                                                                                                |
| MotherCut        | (VFASPF(VCHI2)\<25)                                                                                                                                                      |
| DecayDescriptor  | \[K\*(892)0 -\> K+ pi-\]cc                                                                                                                                               |
| DecayDescriptors | \[\]                                                                                                                                                                     |
| Output           | None                                                                                                                                                                     |
