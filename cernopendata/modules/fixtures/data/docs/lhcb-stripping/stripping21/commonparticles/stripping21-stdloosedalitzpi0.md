[\[stripping21 lines\]](../stripping21-index.md)

# StdLooseDalitzPi0

**CombineParticles/StdLooseDalitzPi0**

|                  |                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdLooseAllPhotons](../commonparticles/stripping21-stdlooseallphotons.md)/Particles', 'Phys/[StdDiElectronGamma](../commonparticles/stripping21-stddielectrongamma.md)/Particles'\] |
| DaughtersCuts    | {}                                                                                                                                                                                           |
| CombinationCut   | ATRUE                                                                                                                                                                                        |
| MotherCut        | (MM \< 170\*MeV) & (MM \> 90\*MeV) & (1 == CHILD(1,cnv)+CHILD(2,cnv) )                                                                                                                       |
| DecayDescriptor  | pi0 -\> gamma gamma                                                                                                                                                                          |
| DecayDescriptors | \[\]                                                                                                                                                                                         |
| Output           | None                                                                                                                                                                                         |
