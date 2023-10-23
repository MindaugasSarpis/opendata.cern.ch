[\[stripping21 lines\]](../stripping21-index.md)

# StdLooseDstarWithD02KK

**CombineParticles/StdLooseDstarWithD02KK**

|                  |                                                                                                                                                                                |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | \['Phys/[StdAllLoosePions](../commonparticles/stripping21-stdallloosepions.md)/Particles', 'Phys/[StdLooseD02KK](../commonparticles/stripping21-stdloosed02kk.md)/Particles'\] |
| DaughtersCuts    | {}                                                                                                                                                                             |
| CombinationCut   | (ADAMASS('D\*(2010)+')\<50\*MeV) & (APT\>1250\*MeV)                                                                                                                            |
| MotherCut        | (VFASPF(VCHI2/VDOF)\<25) & (M-MAXTREE('D0'==ABSID,M)\<165.5)                                                                                                                   |
| DecayDescriptor  | \[D\*(2010)+ -\> pi+ D0\]cc                                                                                                                                                    |
| DecayDescriptors | \[\]                                                                                                                                                                           |
| Output           | None                                                                                                                                                                           |
