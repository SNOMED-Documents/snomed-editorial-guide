# Specimen Attributes Summary

When authoring in this domain, these are the approved attributes and allowable ranges. They are from the Human Readable Concept Model (HRCM). 

HRCM 2025-08-01 

  

## Domain Information for Specimen

| Property | Value |
|---|---|
| Domain Constraint | << 123038009 \| Specimen (specimen) \| |
| Parent Domain | - |
| Proximal Primitive Constraint | << 123038009 \| Specimen (specimen) \| |
| Proximal Primitive Refinement | - |

HRCM 2025-08-01 

  

## Author View of Attributes and Ranges for Specimen

| Attribute | Grouped | Cardinality | In Group Cardinality | Range Constraint |
|---|---|---|---|---|
| 118171006 \| Specimen procedure (attribute) \| | 1 | 0..* | 0..1 | << 71388002 \| Procedure (procedure) \| |
| 118170007 \| Specimen source identity (attribute) \| | 1 | 0..* | 0..1 | << 125676002 \| Person (person) \| OR << 133928008 \| Community (social concept) \| OR << 260787004 \| Physical object (physical object) \| OR << 276339004 \| Environment (environment) \| OR << 35359004 \| Family (social concept) \| |
| 118168003 \| Specimen source morphology (attribute) \| | 1 | 0..* | 0..1 | << 49755003 \| Morphologically abnormal structure (morphologic abnormality) \| |
| 118169006 \| Specimen source topography (attribute) \| | 1 | 0..* | 0..1 | << 442083009 \| Anatomical or acquired body structure (body structure) \| |
| 370133003 \| Specimen substance (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| |

