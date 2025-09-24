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

# Cardiac Valve Prosthesis Naming and Modeling

## Naming

| FSN            | Use the following naming pattern for the FSN; align terming and case sensitivity with the FSN for the concepts selected as the attribute values, excluding the semantic tag. \[is sterile] \[compositional material] \[device intended site] cardiac valve prosthesis (physical object) For example, Biologic cardiac valve prosthesis (physical object) Aortic valve prosthesis (physical object) |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Preferred Term | Use the following naming pattern for the PT; align terming and case sensitivity with the PT for the concept that is selected as the attribute value. \[is sterile] \[compositional material]\[device intended site]cardiac valve prosthesis For example, Biologic cardiac valve prosthesis Aortic valve prosthesis                                                                                 |
| Synonym        | Synonyms are not generally added for concepts in this hierarchy. Exceptions: Heart in place of cardiac , such as in "biologic heart valve prosthesis" "Bioprosthesis" for biologic cardiac valve prosthesis                                                                                                                                                                                        |

## Modeling (stated view)

| Stated parent concept(s)                          | 14789005 \|Prosthetic implant (physical object)\| 303619008 \|Cardiac implant (physical object)\| 705991002 \|Mechanical heart valve prosthesis (physical object)\|, if applicable 258166002 \|Custom made implant (physical object)\|, if applicable                               |
| ------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Semantic tag                                      | (physical object)                                                                                                                                                                                                                                                                   |
| Attribute: Has device intended site (attribute)   | Range: <<123037004 \|Body structure (body structure)\| NOTE: NOTE: While the MRCM allowed range includes the top-level concept, 123037004 \|Body structure (body structure)\|, only the descendants should be used in modeling cardiac valve prosthesis concepts. Cardinality: 0..1 |
| Attribute: Has compositional material (attribute) | Range: <<105590001 \|Substance (substance)\| NOTE: While the MRCM allowed range includes the top-level concept, 105590001 \|Substance (substance)\|, only the descendants should be used in modeling cardiac valve prosthesis concepts. Cardinality: 0..\*                          |
| Attribute: Is sterile (attribute)                 | Range: 31874001 \|True (qualifier value)\| OR 64100000 \|False (qualifier value) Cardinality: 0..1                                                                                                                                                                                  |

## Exemplars

The following illustrates the **stated** view for 736893007 |Aortic tri-leaflet mechanical valve prosthesis (physical object)|:

<figure><img src="../../../../../authoring/physical-object/images/174691277.png" alt=""><figcaption><p>The following illustrates the <strong>inferred</strong> view for 736893007 |Aortic tri-leaflet mechanical valve prosthesis (physical object)|:</p></figcaption></figure>

<figure><img src="../../../../../authoring/physical-object/images/174691278.png" alt=""><figcaption></figcaption></figure>
