[\[stripping21 lines\]](../stripping21-index.md)

# StdVeryLooseDiMuon

**CombineParticles/StdVeryLooseDiMuon**

|                  |                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdAllVeryLooseMuons](../commonparticles/stripping21-stdallveryloosemuons.md)/Particles'\] |
| DaughtersCuts    | {}                                                                                                  |
| CombinationCut   | (ADAMASS('J/psi(1S)') \< 3000.\*MeV) & (ADOCACHI2CUT(30, ''))                                       |
| MotherCut        | (VFASPF(VCHI2) \< 25.)                                                                              |
| DecayDescriptor  | J/psi(1S) -\> mu+ mu-                                                                               |
| DecayDescriptors | \[\]                                                                                                |
| Output           | None                                                                                                |
