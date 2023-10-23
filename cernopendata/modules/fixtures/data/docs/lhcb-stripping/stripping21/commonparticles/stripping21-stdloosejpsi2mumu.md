[\[stripping21 lines\]](../stripping21-index.md)

# StdLooseJpsi2MuMu

**CombineParticles/StdLooseJpsi2MuMu**

|                  |                                                                                             |
|------------------|---------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdAllLooseMuons](../commonparticles/stripping21-stdallloosemuons.md)/Particles'\] |
| DaughtersCuts    | {}                                                                                          |
| CombinationCut   | (ADAMASS('J/psi(1S)') \< 100.\*MeV) & (ADOCACHI2CUT(30,''))                                 |
| MotherCut        | (VFASPF(VCHI2) \< 25.)                                                                      |
| DecayDescriptor  | J/psi(1S) -\> mu+ mu-                                                                       |
| DecayDescriptors | \[\]                                                                                        |
| Output           | None                                                                                        |
