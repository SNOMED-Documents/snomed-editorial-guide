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

# Situation with Explicit Context Attributes Summary

When authoring in this domain, these are the approved attributes and allowable ranges. 


  

## Domain Information for Situation with Explicit Context

| Property | Value |
|---|---|
| Domain Constraint | << 243796009 \| Situation with explicit context (situation) \| |
| Parent Domain | - |
| Proximal Primitive Constraint | << 243796009 \| Situation with explicit context (situation) \| |
| Proximal Primitive Refinement | - |

  

  


  

## Author View of Attributes and Ranges for Situation with Explicit Context

| Attribute | Grouped | Cardinality | In Group Cardinality | Range Constraint |
|---|---|---|---|---|
| 408732007 \| Subject relationship context (attribute) \| | 1 | 0..* | 0..1 | << 125676002 \| Person (person) \| |
| 408731000 \| Temporal context (attribute) \| | 1 | 0..* | 0..1 | << 410510008 \| Temporal context value (qualifier value) \| |


  

## Author View of Attributes and Ranges for Finding with Explicit Context

| Attribute | Grouped | Cardinality | In Group Cardinality | Range Constraint |
|---|---|---|---|---|
| 246090004 \| Associated finding (attribute) \| | 1 | 0..* | 0..1 | << 272379006 \| Event (event) \| OR << 404684003 \| Clinical finding (finding) \| |
| 408729009 \| Finding context (attribute) \| | 1 | 0..* | 0..1 | << 410514004 \| Finding context value (qualifier value) \| |


  

## Author View of Attributes and Ranges for Procedure with Explicit Context

| Attribute | Grouped | Cardinality | In Group Cardinality | Range Constraint |
|---|---|---|---|---|
| 363589002 \| Associated procedure (attribute) \| | 1 | 0..* | 0..1 | << 71388002 \| Procedure (procedure) \| |
| 408730004 \| Procedure context (attribute) \| | 1 | 0..* | 0..1 | << 288532009 \| Context values for actions (qualifier value) \| |

