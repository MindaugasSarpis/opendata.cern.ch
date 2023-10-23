[\[stripping21 lines\]](../stripping21-index.md)

# StrippingWMuLowLine

## Properties:

|                |                           |
|----------------|---------------------------|
| OutputLocation | Phys/WMuLowLine/Particles |
| Postscale      | 1.0000000                 |
| HLT            | None                      |
| Prescale       | 0.10000000                |
| L0DU           | None                      |
| ODIN           | None                      |

## Filter sequence:

CheckPV/checkPVmin0

|        |     |
|--------|-----|
| MinPVs | 0   |
| MaxPVs | -1  |

LoKi::VoidFilter/SelFilterPhys_StdAllLooseMuons_Particles

|      |                                                                                                      |
|------|------------------------------------------------------------------------------------------------------|
| Code | CONTAINS('Phys/[StdAllLooseMuons](../commonparticles/stripping21-stdallloosemuons.md)/Particles')\>0 |

FilterDesktop/WMuLowLine

|                 |                                                                                     |
|-----------------|-------------------------------------------------------------------------------------|
| Code            | (PT\>15.0\*GeV)                                                                     |
| Inputs          | \[ 'Phys/[StdAllLooseMuons](../commonparticles/stripping21-stdallloosemuons.md)' \] |
| DecayDescriptor | None                                                                                |
| Output          | Phys/WMuLowLine/Particles                                                           |
