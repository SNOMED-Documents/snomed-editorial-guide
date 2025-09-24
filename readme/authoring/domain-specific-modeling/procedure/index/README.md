# Procedure Attributes Summary

When authoring in this domain, these are the approved attributes and allowable ranges.

[386053000 | Evaluation procedure (procedure)|](http://snomed.info/id/386053000) , and [387713003 | Surgical procedure (procedure)|](http://snomed.info/id/387713003) each have unique defining attributes as seen in their separate tables below.

## Domain Information for Procedure

| Property                      | Value                                   |
| ----------------------------- | --------------------------------------- |
| Domain Constraint             | << 71388002 \| Procedure (procedure) \| |
| Parent Domain                 | -                                       |
| Proximal Primitive Constraint | << 71388002 \| Procedure (procedure) \| |
| Proximal Primitive Refinement | -                                       |

## Author View of Attributes and Ranges for Procedure

| Attribute                                             | Grouped | Cardinality | In Group Cardinality | Range Constraint                                                                                                                                                                     |
| ----------------------------------------------------- | ------- | ----------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 260507000 \| Access (attribute) \|                    | 1       | 0..\*       | 0..1                 | << 309795001 \| Surgical access values (qualifier value) \|                                                                                                                          |
| 363699004 \| Direct device (attribute) \|             | 1       | 0..\*       | 0..1                 | << 49062001 \| Device (physical object) \|                                                                                                                                           |
| 363700003 \| Direct morphology (attribute) \|         | 1       | 0..\*       | 0..1                 | << 49755003 \| Morphologically abnormal structure (morphologic abnormality) \|                                                                                                       |
| 363701004 \| Direct substance (attribute) \|          | 1       | 0..\*       | 0..1                 | << 105590001 \| Substance (substance) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \|                                                                           |
| 363702006 \| Has focus (attribute) \|                 | 1       | 0..\*       | 0..1                 | << 404684003 \| Clinical finding (finding) \| OR << 71388002 \| Procedure (procedure) \|                                                                                             |
| 363703001 \| Has intent (attribute) \|                | 1       | 0..\*       | 0..1                 | << 363675004 \| Intents (nature of procedure values) (qualifier value) \|                                                                                                            |
| 363710007 \| Indirect device (attribute) \|           | 1       | 0..\*       | 0..1                 | << 49062001 \| Device (physical object) \|                                                                                                                                           |
| 363709002 \| Indirect morphology (attribute) \|       | 1       | 0..\*       | 0..1                 | << 49755003 \| Morphologically abnormal structure (morphologic abnormality) \|                                                                                                       |
| 260686004 \| Method (attribute) \|                    | 1       | 0..\*       | 0..1                 | << 129264002 \| Action (qualifier value) \|                                                                                                                                          |
| 246454002 \| Occurrence (attribute) \|                | 1       | 0..\*       | 0..1                 | << 282032007 \| Periods of life (qualifier value) \|                                                                                                                                 |
| 260870009 \| Priority (attribute) \|                  | 1       | 0..\*       | 0..1                 | << 272125009 \| Priorities (qualifier value) \|                                                                                                                                      |
| 116688005 \| Procedure approach (attribute) \|        | 1       | 0..\*       | 0..1                 | << 103379005 \| Procedural approach (qualifier value) \|                                                                                                                             |
| 405815000 \| Procedure device (attribute) \|          | 1       | 0..\*       | 0..\*                | << 49062001 \| Device (physical object) \|                                                                                                                                           |
| 405816004 \| Procedure morphology (attribute) \|      | 1       | 0..\*       | 0..\*                | << 49755003 \| Morphologically abnormal structure (morphologic abnormality) \|                                                                                                       |
| 363704007 \| Procedure site (attribute) \|            | 1       | 0..\*       | 0..\*                | << 442083009 \| Anatomical or acquired body structure (body structure) \|                                                                                                            |
| 405813007 \| Procedure site - Direct (attribute) \|   | 1       | 0..\*       | 0..1                 | << 442083009 \| Anatomical or acquired body structure (body structure) \|                                                                                                            |
| 405814001 \| Procedure site - Indirect (attribute) \| | 1       | 0..\*       | 0..1                 | << 442083009 \| Anatomical or acquired body structure (body structure) \|                                                                                                            |
| 370131001 \| Recipient category (attribute) \|        | 1       | 0..\*       | 0..1                 | << 125676002 \| Person (person) \| OR << 133928008 \| Community (social concept) \| OR << 35359004 \| Family (social concept) \| OR << 389109008 \| Group (social concept) \|        |
| 246513007 \| Revision status (attribute) \|           | 1       | 0..\*       | 0..1                 | << 255231005 \| Revision - value (qualifier value) \| OR << 257958009 \| Part of multistage procedure (qualifier value) \| OR << 261424001 \| Primary operation (qualifier value) \| |
| 410675002 \| Route of administration (attribute) \|   | 1       | 0..\*       | 0..1                 | << 284009009 \| Route of administration value (qualifier value) \|                                                                                                                   |
| 425391005 \| Using access device (attribute) \|       | 1       | 0..\*       | 0..1                 | << 49062001 \| Device (physical object) \|                                                                                                                                           |
| 424226004 \| Using device (attribute) \|              | 1       | 0..\*       | 0..\*                | << 49062001 \| Device (physical object) \|                                                                                                                                           |
| 424244007 \| Using energy (attribute) \|              | 1       | 0..\*       | 0..1                 | << 78621006 \| Physical force (physical force) \|                                                                                                                                    |
| 424361007 \| Using substance (attribute) \|           | 1       | 0..\*       | 0..1                 | << 105590001 \| Substance (substance) \|                                                                                                                                             |

## Domain Information for Evaluation Procedure

| Property                      | Value                                                                                   |
| ----------------------------- | --------------------------------------------------------------------------------------- |
| Domain Constraint             | << 386053000 \| Evaluation procedure (procedure) \|                                     |
| Parent Domain                 | 71388002 \| Procedure (procedure) \|                                                    |
| Proximal Primitive Constraint | << 71388002 \| Procedure (procedure) \|                                                 |
| Proximal Primitive Refinement | \[\[1..\*]] 260686004 \| Method \| = \[\[+id(<< 129265001 \| Evaluation - action \| )]] |

## Author View of Attributes and Ranges for Evaluation Procedure

| Attribute                                      | Grouped | Cardinality | In Group Cardinality | Range Constraint                                                                                                                                                                                                                                                                                                                                                                                                           |
| ---------------------------------------------- | ------- | ----------- | -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 246093002 \| Component (attribute) \|          | 1       | 0..\*       | 0..\*                | << 105590001 \| Substance (substance) \| OR << 123037004 \| Body structure (body structure) \| OR << 123038009 \| Specimen (specimen) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| OR << 419891008 \| Record artifact (record artifact) \| OR << 540091010000105 \| Calculation (calculation) \| |
| 116686009 \| Has specimen (attribute) \|       | 1       | 0..\*       | 0..1                 | << 123038009 \| Specimen (specimen) \|                                                                                                                                                                                                                                                                                                                                                                                     |
| 370129005 \| Measurement method (attribute) \| | 1       | 0..\*       | 0..1                 | << 127789004 \| Laboratory procedure categorized by method (procedure) \|                                                                                                                                                                                                                                                                                                                                                  |
| 370130000 \| Property (attribute) \|           | 1       | 0..1        | 0..1                 | << 118598001 \| Property (qualifier value) \|                                                                                                                                                                                                                                                                                                                                                                              |
| 370132008 \| Scale type (attribute) \|         | 1       | 0..\*       | 0..1                 | << 117364006 \| Narrative value (qualifier value) \| OR << 117444000 \| Text value (qualifier value) \| OR << 26716007 \| Qualitative value (qualifier value) \| OR < 398195001 \| Measurement scales (qualifier value) \|                                                                                                                                                                                                 |
| 370134009 \| Time aspect (attribute) \|        | 1       | 0..1        | 0..1                 | << 7389001 \| Time frame (qualifier value) \|                                                                                                                                                                                                                                                                                                                                                                              |

## Subpages

* [Procedure Defining Attributes](procedure-defining-attributes.md)
* [Procedure Attributes](index/)
