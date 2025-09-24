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

# Vaccine Product Top Level Groupers

## Overview

The following high level vaccine-related grouper concepts are included in the |Medicinal product| hierarchy.

* 787859002 |Vaccine product (medicinal product)|
  * 836368004 |Vaccine product containing bacteria antigen (medicinal product)|
  * 1290123005 |Vaccine product containing protozoa antigen (medicinal product)|
  * 836369007 |Vaccine product containing virus antigen (medicinal product)|

## Modeling

| Stated parent concept            | 763158003 \|Medicinal product (product)                                                                                                                                                                                                                                                |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Semantic tag                     | (medicinal product)                                                                                                                                                                                                                                                                    |
| Definition status                | Defined                                                                                                                                                                                                                                                                                |
| Attribute: Has active ingredient | Range: <<105590001 \|Substance (substance)\| Cardinality: 0..\* Exception:Top level grouper 787859002 \|Vaccine product (medicinal product)\| does not have a Has active ingredient (attribute).                                                                                       |
| Attribute: Plays role            | While the allowed range is broader, top level vaccine-related grouper concepts should have one and only one Plays role (attribute) with attribute value = 318331000221102 \|Active immunity stimulant therapeutic role (role)\|. Range: <<766940004 \|Role (role)\| Cardinality: 0..\* |

## Naming

| FSN            | Vaccine product (medicinal product) Vaccine product containing bacteria antigen (medicinal product) Vaccine product containing virus antigen (medicinal product) Vaccine product containing bacteria and virus antigens (medicinal product) Use the following pattern for the FSN;align naming and case sensitivity with the PT for the concept that is selected as the attribute value for the 127489000 \|Has active ingredient (attribute)\|. Vaccine product containing\<Active ingredient PT excluding "antigen">antigen(medicinal product) Vaccine product containing\<Active ingredient PTexcluding"antigen">and\<Active ingredient PTexcluding"antigen">antigens(medicinal product) For example, |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Preferred Term | Vaccine product Bacteria antigen-containing vaccine product Virus antigen-containing vaccine product Bacteria- and virus antigens-containing vaccine product Use the following pattern for the PT; align naming and case significance with the PT for the concept that is selected as the attribute value for the 127489000 \|Has active ingredient (attribute)\|. \<Active ingredient PTexcluding "antigen">-containingvaccineproduct \<Active ingredient PTexcluding "antigen">- and\<Active ingredient PTexcluding "antigen">antigens-containingvaccineproduct For example,                                                                                                                           |
| Synonyms       | Synonyms matching the FSN are not required.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## Exemplars

The following illustrates the **stated** view for 787859002 |Vaccine product (product)|:

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690916.png" alt=""><figcaption><p>The following illustrates the <strong>inferred</strong> view for 787859002 |Vaccine product (product)|:</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690915.png" alt=""><figcaption><p>The following illustrates the <strong>stated</strong> view for 836368004 |Vaccine product containing bacteria antigen (medicinal product)|:</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690914.png" alt=""><figcaption><p>The following illustrates the <strong>inferred</strong> view for 836368004 |Vaccine product containing bacteria antigen (medicinal product)|:</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690913.png" alt=""><figcaption><p>The following illustrates the <strong>stated</strong> view for 863950005 |Vaccine product containing bacteria and virus antigens (medicinal product)|:</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690910.png" alt=""><figcaption><p>The following illustrates the <strong>inferred</strong> view for 863950005 |Vaccine product containing bacteria and virus antigens (medicinal product)|:</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690909.png" alt=""><figcaption></figcaption></figure>
