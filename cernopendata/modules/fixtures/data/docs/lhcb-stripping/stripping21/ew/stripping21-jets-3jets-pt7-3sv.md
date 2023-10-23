[\[stripping21 lines\]](../stripping21-index.md)

# StrippingJets_3jets_Pt7_3sv

## Properties:

|                |                                    |
|----------------|------------------------------------|
| OutputLocation | Phys/Jets_3jets_Pt7_3sv/Particles  |
| Postscale      | 1.0000000                          |
| HLT            | HLT_PASS_RE('Hlt2Topo.\*Decision') |
| Prescale       | 1.0000000                          |
| L0DU           | None                               |
| ODIN           | None                               |

## Filter sequence:

CheckPV/checkPVmin1

|        |     |
|--------|-----|
| MinPVs | 1   |
| MaxPVs | -1  |

LoKi::VoidFilter/SelFilterPhys_StdJets_Particles

|      |                                                                                    |
|------|------------------------------------------------------------------------------------|
| Code | CONTAINS('Phys/[StdJets](../commonparticles/stripping21-stdjets.md)/Particles')\>0 |

FilterDesktop/Jets5000.0GeVJets

|                 |                                                                   |
|-----------------|-------------------------------------------------------------------|
| Code            | (PT \> 5000.0)                                                    |
| Inputs          | \[ 'Phys/[StdJets](../commonparticles/stripping21-stdjets.md)' \] |
| DecayDescriptor | None                                                              |
| Output          | Phys/Jets5000.0GeVJets/Particles                                  |

GaudiSequencer/SeqJetsmerged

GaudiSequencer/SEQ:Jets5000.0GeVJets

LoKi::VoidFilter/SelFilterPhys_StdJets_Particles

|      |                                                                                    |
|------|------------------------------------------------------------------------------------|
| Code | CONTAINS('Phys/[StdJets](../commonparticles/stripping21-stdjets.md)/Particles')\>0 |

FilterDesktop/Jets5000.0GeVJets

|                 |                                                                   |
|-----------------|-------------------------------------------------------------------|
| Code            | (PT \> 5000.0)                                                    |
| Inputs          | \[ 'Phys/[StdJets](../commonparticles/stripping21-stdjets.md)' \] |
| DecayDescriptor | None                                                              |
| Output          | Phys/Jets5000.0GeVJets/Particles                                  |

|                    |       |
|--------------------|-------|
| ModeOR             | False |
| IgnoreFilterPassed | False |

GaudiSequencer/SEQ:JetsSvrsSelection

LoKi::VoidFilter/SelFilterPhys_StdAllNoPIDsPions_Particles

|      |                                                                                                        |
|------|--------------------------------------------------------------------------------------------------------|
| Code | CONTAINS('Phys/[StdAllNoPIDsPions](../commonparticles/stripping21-stdallnopidspions.md)/Particles')\>0 |

FilterDesktop/JetsTrksSelection

|                 |                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------|
| Code            | (PT \> 500.0) & (P \> 5000.0) & (MIPCHI2DV(PRIMARY) \> 16) & (TRGHP \< 0.4) & (PPINFO(705,-1) \< 0.7) |
| Inputs          | \[ 'Phys/[StdAllNoPIDsPions](../commonparticles/stripping21-stdallnopidspions.md)' \]                 |
| DecayDescriptor | None                                                                                                  |
| Output          | Phys/JetsTrksSelection/Particles                                                                      |

CombineParticles/JetsSvrsSelection

|                  |                                                              |
|------------------|--------------------------------------------------------------|
| Inputs           | \[ 'Phys/JetsTrksSelection' \]                               |
| DaughtersCuts    | { '' : 'ALL' , 'pi+' : 'ALL' , 'pi-' : 'ALL' }               |
| CombinationCut   | (ADOCACHI2CUT(8,'')) & (AM \< 7000.0) & (ASUM(PT) \> 2000.0) |
| MotherCut        | (BPVDIRA \> 0) & (BPVVDCHI2 \> 100) & (VFASPF(VCHI2) \< 8)   |
| DecayDescriptor  | None                                                         |
| DecayDescriptors | \[ 'D0 -\> pi- pi+' , 'D0 -\> pi- pi-' , 'D0 -\> pi+ pi+' \] |
| Output           | Phys/JetsSvrsSelection/Particles                             |

|                    |       |
|--------------------|-------|
| ModeOR             | False |
| IgnoreFilterPassed | False |

FilterDesktop/Jetsmerged

|                 |                                                           |
|-----------------|-----------------------------------------------------------|
| Code            | ALL                                                       |
| Inputs          | \[ 'Phys/Jets5000.0GeVJets' , 'Phys/JetsSvrsSelection' \] |
| DecayDescriptor | None                                                      |
| Output          | Phys/Jetsmerged/Particles                                 |

|                    |       |
|--------------------|-------|
| ModeOR             | True  |
| IgnoreFilterPassed | False |

TopologicalTagging/JetsbJets

|                 |                          |
|-----------------|--------------------------|
| Inputs          | \[ 'Phys/Jetsmerged' \]  |
| DecayDescriptor | None                     |
| Output          | Phys/JetsbJets/Particles |

TriggerTisTos

|                                 |                                                                                                           |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|
| StatTableHeader :               | \| Counter \| \# \| sum \| mean/eff^\* \| rms/err^\* \| min \| max \|                                     |
| UseParticle2LHCbIDsMap :        | 1                                                                                                         |
| AllowIntermediateSelections :   | False                                                                                                     |
| Particle2LHCbIDsMapLocation :   | None                                                                                                      |
| CompositeTPSviaPartialTOSonly : | False                                                                                                     |
| TriggerInputWarnings :          | False                                                                                                     |
| StatEntityList :                | \[ \]                                                                                                     |
| RootOnTES :                     | None                                                                                                      |
| CaloClustForCharged :           | True                                                                                                      |
| TOSFracTT :                     | 0.0000000                                                                                                 |
| TISFracEcal :                   | 0.0099000000                                                                                              |
| TOSFracHcal :                   | 0.010000000                                                                                               |
| RootInTES :                     | None                                                                                                      |
| HltSelReportsLocation :         | Hlt/SelReports                                                                                            |
| AuditFinalize :                 | False                                                                                                     |
| TISFracVelo :                   | 0.010000000                                                                                               |
| ProjectTracksToCalo :           | True                                                                                                      |
| ErrorsPrint :                   | True                                                                                                      |
| ContextService :                | AlgContextSvc                                                                                             |
| AuditTools :                    | False                                                                                                     |
| HltDecReportsLocation :         | Hlt/DecReports                                                                                            |
| TISFracTT :                     | 0.010000000                                                                                               |
| MonitorService :                | MonitorSvc                                                                                                |
| AuditInitialize :               | False                                                                                                     |
| RegularRowFormat :              | \| %\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.7g\| \|%\|#11.5g\| \|%\|#11.5g\| \|%\|#12.5g\| \|%\|#12.5g\| \| |
| CaloClustForNeutral :           | True                                                                                                      |
| TypePrint :                     | True                                                                                                      |
| StatPrint :                     | True                                                                                                      |
| TISFracMuon :                   | 0.00010000000                                                                                             |
| TISFracHcal :                   | 0.0099000000                                                                                              |
| AuditStop :                     | False                                                                                                     |
| Context :                       | None                                                                                                      |
| PropertiesPrint :               | False                                                                                                     |
| GlobalTimeOffset :              | 0.0000000                                                                                                 |
| UseEfficiencyRowFormat :        | True                                                                                                      |
| OutputLevel :                   | 3                                                                                                         |
| TOSFracEcal :                   | 0.010000000                                                                                               |
| TOSFracMuon :                   | 0.00010000000                                                                                             |
| AuditStart :                    | False                                                                                                     |
| NoHitTypes :                    | False                                                                                                     |
| TISFracOTIT :                   | 0.010000000                                                                                               |
| TOSFracOTIT :                   | 0.70000000                                                                                                |
| TOSFracVelo :                   | 0.70000000                                                                                                |
| EfficiencyRowFormat :           | \|\*%\|-48.48s\|%\|50t\|\|%\|10d\| \|%\|11.5g\| \|(%\|#9.6g\| +- %\|-#9.6g\|)%%\| ------- \| ------- \|   |
| FullAnalysisReport :            | True                                                                                                      |
| CounterList :                   | \[ '.\*' \]                                                                                               |

CombineParticles/Jets_3jets_Pt7_3sv

|                  |                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | \[ 'Phys/Jets5000.0GeVJets' , 'Phys/JetsbJets' \]                                                                                                   |
| DaughtersCuts    | { '' : 'ALL' , 'CELLjet' : '(PT \> 7000.0)' }                                                                                                       |
| CombinationCut   | (abs(ACHILD(BPV(VZ),1)-ACHILD(BPV(VZ),2))\<1\*mm) & (abs(ACHILD(BPV(VZ),1)-ACHILD(BPV(VZ),3))\<1\*mm)                                               |
| MotherCut        | ((INTREE((ABSID=='CELLjet')&(PT\>0.0)))&(INTREE((ABSID=='CELLjet')&(PINFO(9990,0)\>0)))&(2.5 \< NINTREE((ABSID=='CELLjet')&(PINFO(9991,0) \> 5 )))) |
| DecayDescriptor  | H_10 -\> CELLjet CELLjet CELLjet                                                                                                                    |
| DecayDescriptors | \[ 'H_10 -\> CELLjet CELLjet CELLjet' \]                                                                                                            |
| Output           | Phys/Jets_3jets_Pt7_3sv/Particles                                                                                                                   |
