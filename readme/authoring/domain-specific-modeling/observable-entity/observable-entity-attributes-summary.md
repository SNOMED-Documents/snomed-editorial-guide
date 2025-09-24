---
layout:
  width: wide
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Observable Entity Attributes Summary

When authoring in this domain, these are the approved attributes and allowable ranges. 


  

## Domain Information for Observable Entity

| Property | Value |
|---|---|
| Domain Constraint | << 363787002 \| Observable entity (observable entity) \| |
| Parent Domain | - |
| Proximal Primitive Constraint | << 363787002 \| Observable entity (observable entity) \| |
| Proximal Primitive Refinement | - |


  

## Author View of Attributes and Ranges for Observable Entity

| Attribute | Grouped | Cardinality | In Group Cardinality | Range Constraint |
|---|---|---|---|---|
| 704321009 \| Characterizes (attribute) \| | 1 | 0..* | 0..* | << 71388002 \| Procedure (procedure) \| OR << 719982003 \| Process (qualifier value) \| |
| 246093002 \| Component (attribute) \| | 1 | 0..* | 0..* | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 123038009 \| Specimen (specimen) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| OR << 419891008 \| Record artifact (record artifact) \| OR << 540091010000105 \| Calculation (calculation) \| |
| 704327008 \| Direct site (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 123038009 \| Specimen (specimen) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| OR << 419891008 \| Record artifact (record artifact) \| |
| 719722006 \| Has realization (attribute) \| | 1 | 0..* | 0..1 | << 272379006 \| Event (event) \| OR << 404684003 \| Clinical finding (finding) \| OR << 71388002 \| Procedure (procedure) \| OR << 719982003 \| Process (qualifier value) \| |
| 718497002 \| Inherent location (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 123038009 \| Specimen (specimen) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| OR << 419891008 \| Record artifact (record artifact) \| |
| 704319004 \| Inheres in (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 123038009 \| Specimen (specimen) \| OR << 125676002 \| Person (person) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| OR << 419891008 \| Record artifact (record artifact) \| |
| 704326004 \| Precondition (attribute) \| | 1 | 0..* | 0..* | << 404684003 \| Clinical finding (finding) \| OR << 703763000 \| Precondition value (qualifier value) \| OR << 71388002 \| Procedure (procedure) \| |
| 405815000 \| Procedure device (attribute) \| | 1 | 0..* | 0..1 | << 49062001 \| Device (physical object) \| |
| 1003735000 \| Process acts on (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| |
| 704322002 \| Process agent (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| |
| 704323007 \| Process duration (attribute) \| | 1 | 0..* | 0..1 | << 7389001 \| Time frame (qualifier value) \| |
| 1003703000 \| Process extends to (attribute) \| | 1 | 0..* | 0..1 | << 123037004 \| Body structure (body structure) \| |
| 704324001 \| Process output (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 719982003 \| Process (qualifier value) \| |
| 370130000 \| Property (attribute) \| | 1 | 0..* | 0..1 | << 118598001 \| Property (qualifier value) \| |
| 704325000 \| Relative to (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 123038009 \| Specimen (specimen) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| OR << 419891008 \| Record artifact (record artifact) \| |
| 719715003 \| Relative to part of (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 123038009 \| Specimen (specimen) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| OR << 419891008 \| Record artifact (record artifact) \| |
| 370132008 \| Scale type (attribute) \| | 1 | 0..* | 0..1 | << 117364006 \| Narrative value (qualifier value) \| OR << 117444000 \| Text value (qualifier value) \| OR << 26716007 \| Qualitative value (qualifier value) \| OR < 398195001 \| Measurement scales (qualifier value) \| |
| 246501002 \| Technique (attribute) \| | 1 | 0..* | 0..* | << 254291000 \| Staging and scales (staging scale) \| OR << 272394005 \| Technique (qualifier value) \| |
| 370134009 \| Time aspect (attribute) \| | 1 | 0..* | 0..1 | << 7389001 \| Time frame (qualifier value) \| |
| 704320005 \| Towards (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 123038009 \| Specimen (specimen) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| OR << 419891008 \| Record artifact (record artifact) \| |
| 246514001 \| Units (attribute) \| | 1 | 0..* | 0..1 | < 767524001 \| Unit of measure (qualifier value) \| |
| 424226004 \| Using device (attribute) \| | 1 | 0..* | 0..1 | << 49062001 \| Device (physical object) \| |

  

