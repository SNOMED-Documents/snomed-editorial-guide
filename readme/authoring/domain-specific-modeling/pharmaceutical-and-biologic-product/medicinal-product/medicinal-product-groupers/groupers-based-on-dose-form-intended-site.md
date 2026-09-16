---
layout:
  width: default
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
    visible: false
  tags:
    visible: true
  actions:
    visible: true
  anchors:
    visible: true
---

# Groupers Based on Dose form intended site

## Overview

Groupers based on "Dose form intended site" that can be sufficiently defined may be included in the 763158003 |Medicinal product (product)| hierarchy.

* For example,
  * Product manufactured as oral dose form (product)
  * Product manufactured as parenteral dose form (product)

## Naming

### FSN

Product manufactured as \<Manufactured dose form FSN> (product)

For example,

* Product manufactured as oral dose form (product)
* Product manufactured as parenteral dose form (product)

Align naming and case significance with the FSN for the concepts that are selected as the attribute value, excluding the semantic tag.

### Preferred Term

Product manufactured as \<Manufactured dose form PT>

For example,

* Product manufactured as oral dose form
* Product manufactured as parenteral dose form

Align naming and case significance with the PT for the concept that is selected as the attribute value.

### Synonym

Synonyms are not generally created.

## Modeling

| **Stated parent**                                                                    | `763158003 \|Medicinal product (product)` |
| ------------------------------------------------------------------------------------ | ----------------------------------------- |
| **Semantic tag**                                                                     | (product)                                 |
| **Definition status**                                                                | Defined                                   |
| <p><strong>Attribute:</strong></p><p><strong>Has manufactured dose form</strong></p> | Range: `<<736542009`                      |

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/image (41) (1).png" alt=""><figcaption><p><strong>Stated and inferred</strong> view for 440131009 |Product manufactured as oral dose form (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (42) (1).png" alt=""><figcaption><p><strong>Stated and inferred</strong> view for 440132002 |Product manufactured as parenteral dose form (product)|</p></figcaption></figure>

<figure><img src="https://github.com/SNOMED-Documents/snomed-editorial-guide/blob/main/authoring/pharmaceutical-and-biologic-product/images/174690977.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Groupers%20Based%20on%20Dose%20form%20intended%20site" class="button primary">Provide Feedback</a>
