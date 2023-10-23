[\[stripping21 lines\]](../stripping21-index.md)

# StdLoosePi02gee

**CombineParticles/StdLoosePi02gee**

|                  |                                                                                                                                                                                                                                                                                           |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdLooseAllPhotons](../commonparticles/stripping21-stdlooseallphotons.md)/Particles', 'Phys/[StdAllLooseGammaLL](../commonparticles/stripping21-stdallloosegammall.md)/Particles', 'Phys/[StdAllLooseGammaDD](../commonparticles/stripping21-stdallloosegammadd.md)/Particles'\] |
| DaughtersCuts    | {}                                                                                                                                                                                                                                                                                        |
| CombinationCut   | ATRUE                                                                                                                                                                                                                                                                                     |
| MotherCut        | (MM \< 170\*MeV) & (MM \> 90\*MeV) & (1 == CHILD(1,cnv)+CHILD(2,cnv) )                                                                                                                                                                                                                    |
| DecayDescriptor  | pi0 -\> gamma gamma                                                                                                                                                                                                                                                                       |
| DecayDescriptors | \[\]                                                                                                                                                                                                                                                                                      |
| Output           | None                                                                                                                                                                                                                                                                                      |
