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

# Pharmaceutical Dose Form

## Describing Dose forms

A Clinical Drug concept has a pharmaceutical dose form, the physical manifestation of a medicinal product that contains the active ingredient substance(s) and inactive ingredient substances that are intended for administration for the patient. The Clinical Drug concept in the international release is defined by its manufactured dose form, the dose form as the item is presented by the manufacturer into the supply chain. This may be the same as the administrable dose form, which is the dose form that can be given to the patient after any necessary transformation (such as dissolution or dispersion) has taken place. or it may be different. Examples of the relationship between manufactured and administrable dose forms and transformation are given below. Note that both manufactured dose forms and administrable dose forms are types of pharmaceutical dose form.

| Manufactured dose form                                                        | Administrable dose form                    | Transformation |
| ----------------------------------------------------------------------------- | ------------------------------------------ | -------------- |
| conventional release oral tablet                                              | conventional release oral tablet           | none           |
| tablet for conventional release oral solution (synonym "soluble oral tablet") | oral solution                              | dissolve       |
| conventional release cutaneous cream                                          | conventional release cutaneous cream       | none           |
| powder for prolonged-release suspension for injection                         | prolonged-release suspension for injection | disperse       |

The exception to the principle of using the manufactured dose form to describe Clinical Drugs in the international release is for oral antimicrobial liquid products (solutions, suspensions) that are supplied by the manufacturer as powders but undergo dissolution or dispersion prior to dispensing for administration. The exception is because of the need to describe these products using a clinically relevant strength reflecting the concentration of the administered liquid.

## General Assumptions and Requirements

Concept model will include attributes necessary to define the concepts to ensure consistent and reproducible modeling of concepts, whose use is primarily to describe or group concepts in the [763158003 | Medicinal product (product)|](http://snomed.info/id/763158003) hierarchy.

Any requirement to align to external standards or registries will be explicitly documented.

Concept model will be compatible with the following ISO (International Organization for Standardization) IDMP (Identification of Medicinal Products) standards where appropriate:

* ISO 11239 Health informatics, Data elements and structures for the unique identification and exchange of regulated information on pharmaceutical dose forms, units of presentation, routes of administration and packaging
* ISO/TS 20440 Health informatics, Implementation guide for ISO 11239 data elements and structures for the unique identification and exchange of regulated information on pharmaceutical dose forms, units of presentation, routes of administration and packaging

Concepts in the 736542009 |Pharmaceutical dose form (dose form)| hierarchy:

* shall be sufficiently defined using proximal primitive modeling methodology unless explicitly noted as an exception in the editorial guidelines,
* is not intended to eliminate the need for a national extension.

## Out of Scope

* Concepts representing combined pharmaceutical dose forms
  * single concepts describing the multiple dose forms found in kit products such as cream and pessary
  * two pharmaceutical dose forms are put together like powder and solvent for solution for injection
* Concepts in pattern "x for y for z" (e.g. Powder for concentrate for dispersion for infusion)
* Concepts representing proprietary dose forms

Concepts that are not allowed to be used in modeling Medicinal product concepts in the International Release may be added to the Pharmaceutical dose form hierarchy to support national extension modeling.

For example,

* 420378007 |Prolonged-release film-coated oral tablet (dose form)|)

## Overview

The 736542009 |Pharmaceutical dose form (dose form)| hierarchy is comprised of the types of concepts as shown in the table below. Detailed editorial guidelines for each distinct concept type, including required attributes and naming guidelines, are found in the sections that follow.

For the purposes of the following editorial guidelines, pharmaceutical dose form refers to the physical manifestation of a medicinal product that contains the active ingredient substance(s) and inactive ingredient substances that are intended for administration for the patient.

| Concept type                            | Examples                                                                                                                                                                           |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Grouper based on intended site          | 740596000 \|Cutaneous dose form (dose form)\| 385268001 \|Oral dose form (dose form)\|                                                                                             |
| Grouper concept without basic dose form | 385105007 \|Conventional release cutaneous spray (dose form) \| 385136004 \|Conventional release ear drops (dose form)\|                                                           |
| Pharmaceutical dose form                | 385151008 \|Conventional release nasal ointment (dose form) \| 421026006 \|Conventional release oral tablet (dose form)\| 385053008 \|Prolonged-release oral capsule (dose form)\| |

## Dose form intended site vs. Route of administration

The following definitions explain the differences between dose form intended site and route of administration:

736474004 |Has dose form intended site (attribute)|

* Dose form intended site describes the general anatomic location that the dose form has been formulated for administration to or at. The intended site is not intended to describe a precise site or route of administration. For example, eye drops (prepared for ocular intended site) are subject to pharmacopoeial standards for pH and sterility.

410675002 |Route of administration (attribute)|

* The route of administration is the path by which the product is taken into, or makes contact with, the body and is a property of the administration action. The route of administration of a medication is determined by the prescriber in their prescription dosage instructions for a particular patient.

736479009 |Dose form intended site (intended site)|

* The set of values for dose form intended site that relate to characteristics associated with a pharmaceutical dose form and do not refer to a precise anatomic location.

284009009 |Route of administration value (qualifier value)|

* The set of values for route of administration. For medicinal products, these values are associated with the action of administration.

## Multiple\*\*\*\* intended sites and administration methods

Pharmaceutical dose forms with two or more intended sites will use “and” in their terming and include all intended sites in the model. Representing combinations of intended sites as a conjunction ('and' in the description) will facilitate searching by end users. The concepts are logically modeled as conjunction.

Pharmaceutical dose forms with two or more administration methods is a less common requirement, thus requests for this type of dose form are reviewed on a case by case basis.

## Subpages

* [Pharmaceutical Dose Form Naming and Modeling Conventions](pharmaceutical-dose-form-naming-and-modeling-conventions.md)
* [Pharmaceutical Dose Form Grouper Based on Intended Site](pharmaceutical-dose-form-grouper-based-on-intended-site.md)
* [Pharmaceutical Dose Form Grouper Without Basic Dose Form](pharmaceutical-dose-form-grouper-without-basic-dose-form.md)
* [Pharmaceutical Dose Form Supporting Hierarchies](index/)
