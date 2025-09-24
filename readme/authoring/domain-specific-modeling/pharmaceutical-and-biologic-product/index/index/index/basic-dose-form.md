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

# Basic Dose Form

## Overview

The basic dose form represents a general type of pharmaceutical formulation (e.g. tablet, capsule, cream, ointment, solution, emulsion) used for medicinal products. To support fully defining concepts in the 736542009 |Pharmaceutical dose form (dose form)| hierarchy, a hierarchy representing basic dose form is required.

Concepts in the 736478001 |Basic dose form (basic dose form)| hierarchy will be used to model concepts in the 736542009 |Pharmaceutical dose form (dose form)| hierarchy; they will not be used to model concepts in the 763158003 |Medicinal product (product)| hierarchy.

The 736478001 |Basic dose form (basic dose form)| hierarchy is a descendant of 362981000 |Qualifier value (qualifier value)|.

## Modeling

Descendants shall be modeled as follows.

| Parent concept                             | 736478001 \|Bas ic dose form (basic dose form)                                                       |
| ------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| Semantic tag                               | (basic dose form)                                                                                    |
| Definition status                          | Primitive Exceptions: Grouper concepts based on state of matter shall have Defined definition status |
| Attribute: Has state of matter (attribute) | Range: <736471007 \|State of matter (state of matter) Cardinality: 1..1                              |

## Naming Guidelines for Grouper Concept

| FSN              | Basic dose form with state of matter (basic dose form) Basic dose form with liquid state of matter (basic dose form) Basic dose form with solid state of matter (basic dose form) Use the following pattern for the FSN; align naming and case sensitivity with the FSN for the concept that is selected as the attribute value, excluding the semantic tag. For example, |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Preferred Term   | state of matter Liquid dose form Solid dose form Use the following pattern for the PT; align naming and case sensitivity with the PT for the concept that is selected as the attribute value. For example,                                                                                                                                                                |
| Synonyms         | A synonym to match the FSN is required. Additional synonyms are not allowed unless explicitly identified as an exception in the Editorial Guidelines.                                                                                                                                                                                                                     |
| Text Definitions | Preferred; not required.                                                                                                                                                                                                                                                                                                                                                  |

## Exemplars for Grouper Concept

The following illustrates the **stated** view for 420699003 |Basic dose form with liquid state of matter (basic dose form)|:\*\*\
\*\*

<figure><img src="../../../../../../../authoring/pharmaceutical-and-biologic-product/images/174691162.png" alt=""><figcaption><p>The following illustrates the *<em><strong>inferred</strong></em> *view for 420699003 |Basic dose form with liquid state of matter (basic dose form)|:</p></figcaption></figure>

<figure><img src="../../../../../../../authoring/pharmaceutical-and-biologic-product/images/174691158.png" alt=""><figcaption></figcaption></figure>

## Naming Guidelines for Basic Dose Form Concept

| FSN              | X (basic dose form) Cream (basic dose form) Gel (basic dose form) Suppository (basic dose form) Tablet (basic dose form) Plural form to be used for Granules (basic dose form) Use the following pattern for the FSN where X is the basic dose form: For example, Exceptions: |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Preferred Term   | X Cream Gel Suppository Tablet Plural form to be used for Granules Use the following pattern for the PTwhere X is the basic dose form: For example, Exceptions:                                                                                                               |
| Synonyms         | Synonyms are not allowed unless explicitly identified as an exception in the Editorial Guidelines.                                                                                                                                                                            |
| Text Definitions | Text definitions are not required but are encouraged.                                                                                                                                                                                                                         |

## Exemplars for Basic Dose Form Concept

The following illustrates the **stated** view for 739006009 |Solution (basic dose form)|:

<figure><img src="../../../../../../../authoring/pharmaceutical-and-biologic-product/images/174691160.png" alt=""><figcaption><p>The following illustrates the <strong>inferred</strong> view for 739006009 |Solution (basic dose form)|:</p></figcaption></figure>

<figure><img src="../../../../../../../authoring/pharmaceutical-and-biologic-product/images/174691159.png" alt=""><figcaption></figcaption></figure>
