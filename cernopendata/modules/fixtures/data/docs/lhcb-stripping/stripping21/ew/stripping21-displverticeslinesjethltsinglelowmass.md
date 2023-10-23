[\[stripping21 lines\]](../stripping21-index.md)

# StrippingDisplVerticesLinesJetHltSingleLowMass

## Properties:

|                |                                                      |
|----------------|------------------------------------------------------|
| OutputLocation | Phys/DisplVerticesLinesJetHltSingleLowMass/Particles |
| Postscale      | 1.0000000                                            |
| HLT            | None                                                 |
| Prescale       | 1.0000000                                            |
| L0DU           | None                                                 |
| ODIN           | None                                                 |

## Filter sequence:

CheckPV/checkPVmin1

|        |     |
|--------|-----|
| MinPVs | 1   |
| MaxPVs | -1  |

GaudiSequencer/DisplVerticesLinesHltCandidates

GaudiSequencer/DisplVerticesLinesHlt2CandFilterTCK0x001c0028-0x002f002c

LoKi::HDRFilter/DisplVerticesLinesHltDecisionFilterTCK0x001c0028-0x002f002c

|      |                                                                                                             |
|------|-------------------------------------------------------------------------------------------------------------|
| Code | in_range( 0x001c0028, HLT_TCK % 0x40000000 , 0x002f002c ) & ( HLT_PASS('Hlt2DisplVerticesSingleDecision') ) |

HltVertexConverterS20p3/DisplVerticesLinesHltConverter0x001c0028-0x002f002c

|                 |                                           |
|-----------------|-------------------------------------------|
| Inputs          | \[ \]                                     |
| DecayDescriptor | None                                      |
| Output          | Phys/DisplVerticesLinesHlt2Cand/Particles |

|                    |       |
|--------------------|-------|
| ModeOR             | False |
| IgnoreFilterPassed | False |

GaudiSequencer/DisplVerticesLinesHlt2CandFilterTCK0x00340032-0x00730035

LoKi::HDRFilter/DisplVerticesLinesHltDecisionFilterTCK0x00340032-0x00730035

|      |                                                                                                                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Code | in_range( 0x00340032, HLT_TCK % 0x40000000 , 0x00730035 ) & ( HLT_PASS('Hlt2DisplVerticesHighFDSingleDecision') \| HLT_PASS('Hlt2DisplVerticesHighMassSingleDecision') \| HLT_PASS('Hlt2DisplVerticesLowMassSingleDecision') \| HLT_PASS('Hlt2DisplVerticesSingleDownDecision') ) |

HltVertexConverterS20p3/DisplVerticesLinesHltConverter0x00340032-0x00730035

|                 |                                           |
|-----------------|-------------------------------------------|
| Inputs          | \[ \]                                     |
| DecayDescriptor | None                                      |
| Output          | Phys/DisplVerticesLinesHlt2Cand/Particles |

|                    |       |
|--------------------|-------|
| ModeOR             | False |
| IgnoreFilterPassed | False |

GaudiSequencer/DisplVerticesLinesHlt2CandFilterTCK0x00750037-0x007b0038

LoKi::HDRFilter/DisplVerticesLinesHltDecisionFilterTCK0x00750037-0x007b0038

|      |                                                                                                                                                                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Code | in_range( 0x00750037, HLT_TCK % 0x40000000 , 0x007b0038 ) & ( HLT_PASS('Hlt2DisplVerticesSingleDecision') \| HLT_PASS('Hlt2DisplVerticesSingleDownDecision') \| HLT_PASS('Hlt2DisplVerticesSingleHighFDPostScaledDecision') \| HLT_PASS('Hlt2DisplVerticesSingleHighMassPostScaledDecision') ) |

HltVertexConverterS20p3/DisplVerticesLinesHltConverter0x00750037-0x007b0038

|                 |                                           |
|-----------------|-------------------------------------------|
| Inputs          | \[ \]                                     |
| DecayDescriptor | None                                      |
| Output          | Phys/DisplVerticesLinesHlt2Cand/Particles |

|                    |       |
|--------------------|-------|
| ModeOR             | False |
| IgnoreFilterPassed | False |

GaudiSequencer/DisplVerticesLinesHlt2CandFilterTCK0x007e0039-0x0097003d

LoKi::HDRFilter/DisplVerticesLinesHltDecisionFilterTCK0x007e0039-0x0097003d

|      |                                                                                                                                                                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Code | in_range( 0x007e0039, HLT_TCK % 0x40000000 , 0x0097003d ) & ( HLT_PASS('Hlt2DisplVerticesSingleDecision') \| HLT_PASS('Hlt2DisplVerticesSingleDownDecision') \| HLT_PASS('Hlt2DisplVerticesSingleHighFDPostScaledDecision') \| HLT_PASS('Hlt2DisplVerticesSingleHighMassPostScaledDecision') ) |

HltVertexConverterS20p3/DisplVerticesLinesHltConverter0x007e0039-0x0097003d

|                 |                                           |
|-----------------|-------------------------------------------|
| Inputs          | \[ \]                                     |
| DecayDescriptor | None                                      |
| Output          | Phys/DisplVerticesLinesHlt2Cand/Particles |

|                    |       |
|--------------------|-------|
| ModeOR             | False |
| IgnoreFilterPassed | False |

GaudiSequencer/DisplVerticesLinesHlt2CandFilterTCK0x00990042-0x40000000

LoKi::HDRFilter/DisplVerticesLinesHltDecisionFilterTCK0x00990042-0x40000000

|      |                                                                                                                                                                                                                                                                                                                                     |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Code | in_range( 0x00990042, HLT_TCK % 0x40000000 , 0x40000000 ) & ( HLT_PASS('Hlt2DisplVerticesSingleDecision') \| HLT_PASS('Hlt2DisplVerticesSingleDownDecision') \| HLT_PASS('Hlt2DisplVerticesSingleHighFDDecision') \| HLT_PASS('Hlt2DisplVerticesSingleHighMassDecision') \| HLT_PASS('Hlt2DisplVerticesSingleVeryHighFDDecision') ) |

HltVertexConverterS20p3/DisplVerticesLinesHltConverter0x00990042-0x40000000

|                 |                                           |
|-----------------|-------------------------------------------|
| Inputs          | \[ \]                                     |
| DecayDescriptor | None                                      |
| Output          | Phys/DisplVerticesLinesHlt2Cand/Particles |

|                    |       |
|--------------------|-------|
| ModeOR             | False |
| IgnoreFilterPassed | False |

|                    |       |
|--------------------|-------|
| ModeOR             | True  |
| IgnoreFilterPassed | False |

LoKi::VoidFilter/SelFilterPhys_DisplVerticesLinesHlt2Cand_Particles

|      |                                                          |
|------|----------------------------------------------------------|
| Code | CONTAINS('Phys/DisplVerticesLinesHlt2Cand/Particles')\>0 |

VeloEventShapeCutsS20p3/DisplVerticesLinesHltVeloGEC

FilterDesktop/DisplVerticesLinesHlt2CandVertices

|                 |                                                   |
|-----------------|---------------------------------------------------|
| Code            | ( ABSID == '~chi_10' )                            |
| Inputs          | \[ 'Phys/DisplVerticesLinesHlt2Cand' \]           |
| DecayDescriptor | None                                              |
| Output          | Phys/DisplVerticesLinesHlt2CandVertices/Particles |

DisplacedVertexJetCandidateMakerS20p3/DisplVerticesLinesJetHltSingleLowMassSelectionHltJets

|                 |                                                                      |
|-----------------|----------------------------------------------------------------------|
| Inputs          | \[ 'Phys/DisplVerticesLinesHlt2CandVertices' \]                      |
| DecayDescriptor | None                                                                 |
| Output          | Phys/DisplVerticesLinesJetHltSingleLowMassSelectionHltJets/Particles |

JEC

|                          |                                                                                                           |
|--------------------------|-----------------------------------------------------------------------------------------------------------|
| StatTableHeader :        | \| Counter \| \# \| sum \| mean/eff^\* \| rms/err^\* \| min \| max \|                                     |
| ErrorsPrint :            | True                                                                                                      |
| StatEntityList :         | \[ \]                                                                                                     |
| RootOnTES :              | None                                                                                                      |
| RootInTES :              | None                                                                                                      |
| AuditFinalize :          | False                                                                                                     |
| TypePrint :              | True                                                                                                      |
| UseEfficiencyRowFormat : | True                                                                                                      |
| ContextService :         | AlgContextSvc                                                                                             |
| AuditTools :             | False                                                                                                     |
| MonitorService :         | MonitorSvc                                                                                                |
| AuditInitialize :        | False                                                                                                     |
| RegularRowFormat :       | \| %\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.7g\| \|%\|#11.5g\| \|%\|#11.5g\| \|%\|#12.5g\| \|%\|#12.5g\| \| |
| OutputLevel :            | 3                                                                                                         |
| StatPrint :              | True                                                                                                      |
| HistoPath :              | DisplVerticesLines_JEC                                                                                    |
| AuditStop :              | False                                                                                                     |
| Context :                | None                                                                                                      |
| PropertiesPrint :        | False                                                                                                     |
| GlobalTimeOffset :       | 0.0000000                                                                                                 |
| ShiftJEC :               | 0.00000                                                                                                   |
| AuditStart :             | False                                                                                                     |
| Apply :                  | False                                                                                                     |
| EfficiencyRowFormat :    | \|\*%\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.5g\| \|(%\|#9.6g\| +- %\|-#9.6g\|)%%\| ------- \| ------- \|   |
| CounterList :            | \[ '.\*' \]                                                                                               |

MomentumCombiner

|                          |                                                                                                           |
|--------------------------|-----------------------------------------------------------------------------------------------------------|
| Transporter :            | None                                                                                                      |
| StatTableHeader :        | \| Counter \| \# \| sum \| mean/eff^\* \| rms/err^\* \| min \| max \|                                     |
| ErrorsPrint :            | True                                                                                                      |
| StatEntityList :         | \[ \]                                                                                                     |
| RootOnTES :              | None                                                                                                      |
| PrintMyAlg :             | True                                                                                                      |
| RootInTES :              | None                                                                                                      |
| AuditFinalize :          | False                                                                                                     |
| TypePrint :              | True                                                                                                      |
| UseEfficiencyRowFormat : | True                                                                                                      |
| ContextService :         | AlgContextSvc                                                                                             |
| AuditTools :             | False                                                                                                     |
| MonitorService :         | MonitorSvc                                                                                                |
| AuditInitialize :        | False                                                                                                     |
| RegularRowFormat :       | \| %\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.7g\| \|%\|#11.5g\| \|%\|#11.5g\| \|%\|#12.5g\| \|%\|#12.5g\| \| |
| OutputLevel :            | 3                                                                                                         |
| StatPrint :              | True                                                                                                      |
| AuditStop :              | False                                                                                                     |
| Context :                | None                                                                                                      |
| PropertiesPrint :        | False                                                                                                     |
| GlobalTimeOffset :       | 0.0000000                                                                                                 |
| AuditStart :             | False                                                                                                     |
| EfficiencyRowFormat :    | \|\*%\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.5g\| \|(%\|#9.6g\| +- %\|-#9.6g\|)%%\| ------- \| ------- \|   |
| CounterList :            | \[ '.\*' \]                                                                                               |

LoKi\_\_FastJetMaker

|                          |                                                                                                           |
|--------------------------|-----------------------------------------------------------------------------------------------------------|
| RParameter :             | 1.2000000                                                                                                 |
| StatTableHeader :        | \| Counter \| \# \| sum \| mean/eff^\* \| rms/err^\* \| min \| max \|                                     |
| Strategy :               | 1                                                                                                         |
| Type :                   | 2                                                                                                         |
| Sort :                   | 2                                                                                                         |
| StatEntityList :         | \[ \]                                                                                                     |
| RootOnTES :              | None                                                                                                      |
| ParticleCombiner :       | MomentumCombiner                                                                                          |
| RootInTES :              | None                                                                                                      |
| AuditFinalize :          | False                                                                                                     |
| TypePrint :              | True                                                                                                      |
| ErrorsPrint :            | True                                                                                                      |
| ContextService :         | AlgContextSvc                                                                                             |
| AuditTools :             | False                                                                                                     |
| MonitorService :         | MonitorSvc                                                                                                |
| AuditInitialize :        | False                                                                                                     |
| RegularRowFormat :       | \| %\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.7g\| \|%\|#11.5g\| \|%\|#11.5g\| \|%\|#12.5g\| \|%\|#12.5g\| \| |
| OutputLevel :            | 3                                                                                                         |
| StatPrint :              | True                                                                                                      |
| JetID :                  | 98                                                                                                        |
| AuditStop :              | False                                                                                                     |
| PtMin :                  | 5000.0000                                                                                                 |
| Context :                | None                                                                                                      |
| PropertiesPrint :        | False                                                                                                     |
| GlobalTimeOffset :       | 0.0000000                                                                                                 |
| UseEfficiencyRowFormat : | True                                                                                                      |
| AuditStart :             | False                                                                                                     |
| Recombination :          | 0                                                                                                         |
| EfficiencyRowFormat :    | \|\*%\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.5g\| \|(%\|#9.6g\| +- %\|-#9.6g\|)%%\| ------- \| ------- \|   |
| CounterList :            | \[ '.\*' \]                                                                                               |

JetIDInfo

|                          |                                                                                                           |
|--------------------------|-----------------------------------------------------------------------------------------------------------|
| StatTableHeader :        | \| Counter \| \# \| sum \| mean/eff^\* \| rms/err^\* \| min \| max \|                                     |
| ErrorsPrint :            | True                                                                                                      |
| StatEntityList :         | \[ \]                                                                                                     |
| RootOnTES :              | None                                                                                                      |
| RootInTES :              | None                                                                                                      |
| AuditFinalize :          | False                                                                                                     |
| TypePrint :              | True                                                                                                      |
| UseEfficiencyRowFormat : | True                                                                                                      |
| ContextService :         | AlgContextSvc                                                                                             |
| AuditTools :             | False                                                                                                     |
| MonitorService :         | MonitorSvc                                                                                                |
| AuditInitialize :        | False                                                                                                     |
| RegularRowFormat :       | \| %\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.7g\| \|%\|#11.5g\| \|%\|#11.5g\| \|%\|#12.5g\| \|%\|#12.5g\| \| |
| OutputLevel :            | 3                                                                                                         |
| StatPrint :              | True                                                                                                      |
| AuditStop :              | False                                                                                                     |
| Context :                | None                                                                                                      |
| PropertiesPrint :        | False                                                                                                     |
| GlobalTimeOffset :       | 0.0000000                                                                                                 |
| AuditStart :             | False                                                                                                     |
| EfficiencyRowFormat :    | \|\*%\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.5g\| \|(%\|#9.6g\| +- %\|-#9.6g\|)%%\| ------- \| ------- \|   |
| CounterList :            | \[ '.\*' \]                                                                                               |

FilterDesktop/DisplVerticesLinesJetHltSingleLowMass

|                 |                                                                    |
|-----------------|--------------------------------------------------------------------|
| Code            | ISLLP & ( MM \> 0.0 )                                              |
| Inputs          | \[ 'Phys/DisplVerticesLinesJetHltSingleLowMassSelectionHltJets' \] |
| DecayDescriptor | ~chi_10                                                            |
| Output          | Phys/DisplVerticesLinesJetHltSingleLowMass/Particles               |

AddRelatedInfo/RelatedInfo1_DisplVerticesLinesJetHltSingleLowMass

|                 |                                                                   |
|-----------------|-------------------------------------------------------------------|
| Inputs          | \[ 'Phys/DisplVerticesLinesJetHltSingleLowMass' \]                |
| DecayDescriptor | None                                                              |
| Output          | Phys/RelatedInfo1_DisplVerticesLinesJetHltSingleLowMass/Particles |

Tool1

|                          |                                                                                                           |
|--------------------------|-----------------------------------------------------------------------------------------------------------|
| StatTableHeader :        | \| Counter \| \# \| sum \| mean/eff^\* \| rms/err^\* \| min \| max \|                                     |
| ErrorsPrint :            | True                                                                                                      |
| StatEntityList :         | \[ \]                                                                                                     |
| RootOnTES :              | None                                                                                                      |
| RootInTES :              | None                                                                                                      |
| AuditFinalize :          | False                                                                                                     |
| TypePrint :              | True                                                                                                      |
| UseEfficiencyRowFormat : | True                                                                                                      |
| ContextService :         | AlgContextSvc                                                                                             |
| AuditTools :             | False                                                                                                     |
| MonitorService :         | MonitorSvc                                                                                                |
| AuditInitialize :        | False                                                                                                     |
| RegularRowFormat :       | \| %\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.7g\| \|%\|#11.5g\| \|%\|#11.5g\| \|%\|#12.5g\| \|%\|#12.5g\| \| |
| OutputLevel :            | 3                                                                                                         |
| StatPrint :              | True                                                                                                      |
| AuditStop :              | False                                                                                                     |
| Context :                | None                                                                                                      |
| PropertiesPrint :        | False                                                                                                     |
| GlobalTimeOffset :       | 0.0000000                                                                                                 |
| AuditStart :             | False                                                                                                     |
| EfficiencyRowFormat :    | \|\*%\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.5g\| \|(%\|#9.6g\| +- %\|-#9.6g\|)%%\| ------- \| ------- \|   |
| CounterList :            | \[ '.\*' \]                                                                                               |
