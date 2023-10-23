[\[stripping21 lines\]](../stripping21-index.md)

# StdLooseKstar2Kpi

**CombineParticles/StdLooseKstar2Kpi**

|                  |                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdAllLooseKaons](../commonparticles/stripping21-stdallloosekaons.md)/Particles', 'Phys/[StdAllLoosePions](../commonparticles/stripping21-stdallloosepions.md)/Particles'\] |
| DaughtersCuts    | {}                                                                                                                                                                                   |
| CombinationCut   | (APT \> 500.\*MeV) & (ADAMASS('K\*(892)0') \< 300.\*MeV) & (ADOCACHI2CUT(30, ''))                                                                                                    |
| MotherCut        | (VFASPF(VCHI2) \< 25.)                                                                                                                                                               |
| DecayDescriptor  | \[K\*(892)0 -\> K+ pi-\]cc                                                                                                                                                           |
| DecayDescriptors | \[\]                                                                                                                                                                                 |
| Output           | None                                                                                                                                                                                 |
