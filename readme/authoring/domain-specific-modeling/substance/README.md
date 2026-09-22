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

# Substance

<table><thead><tr><th width="461.52734375">Definition</th><th>Examples</th></tr></thead><tbody><tr><td><p>The |Substance| hierarchy contains concepts that can be used for recording and modeling: chemical constituents of medicinal and non-medicinal products; allergies, adverse reactions, poisoning; physicians and nursing orders and laboratory reports and results.</p><p></p><p>Subhierarchies of |Substance| include but are not limited to |Body substance (substance)| and |Chemical (substance)|</p></td><td><ul><li>Albumin (substance)</li><li>Amoxicillin (substance)</li><li>Amoxicillin trihydrate (substance)</li><li>Chromatin (substance)</li><li>Endorphin (substance)</li><li>Methane (substance)</li><li>Paracetamol (substance)</li></ul></td></tr></tbody></table>

## General Assumptions and Requirements

Scope of the |Substance| hierarchy in the International Release include substances that support the modeling of concepts in other SNOMED CT hierarchies, such as Medicinal product, Clinical finding, Procedure, Observable Entity, and Specimen.

Decisions regarding requirements, applicable use cases, scope, terming, and modeling guidelines are made based on requests submitted by user community and in consultation with subject matter experts, associated Project Groups, and relevant credible references.

Top level concepts in the hierarchy will primarily be grouper concepts for both the stated and inferred views.

Concepts representing dispositions in the |Substance| hierarchy shall be sufficiently defined using proximal primitive modeling methodology unless explicitly noted as an exception in the editorial guidelines.

## Out of scope

Concepts describing the following are out of scope for the Substance hierarchy.

### Dose form or Route of administration

Concepts that refer to dose form (e.g., solution) or route of administration (e.g., topical)

* Existing instances will be inactivated as nonconformant to editorial policy. Requests for new instances will be rejected.

### Role or Context

Concepts that refer to role or a specific context (e.g., dietary, medicinal, non-pharmaceutical, substance of abuse)

* Existing instances will be kept in the substance hierarchy; however, additional concepts of this type will not be created, and requests for new instances will be rejected.

### Release state

Concepts that refer to a release state (e.g., immediate release, extended release)

* Existing instances will be inactivated as nonconformant to editorial policy. Requests for new instances will be rejected.

### Brand or trade name

Concepts that refer to a brand or trade name

* Existing instances will be inactivated as nonconformant to editorial policy. Requests for new instances will be rejected.

### Base and total descriptions

Concepts that state _total_ due to the inability to differentiate the definition between the _base_ substance and _total_ substance (e.g., _cholesterol_ versus _total cholesterol_) as well as the inability to create an appropriate relationship between the _base_ and _total_ concepts

* Existing instances will be inactivated as nonconformant to editorial policy. Requests for new instances will be rejected.

### Homeopathic products

Substances used in homeopathic products

* Existing instances will be retained for now; however, requests for new instances will be rejected.

### Traditional medicine products

Substances used in traditional medicine products

* Existing instances will be retained for now; however, requests for new instances will be rejected.

### Combinations and mixtures

Concepts that represent a combination of two or more separate substances

* Existing instances have been inactivated. Changes to SNOMED CT concept model to permit the use of concepts within the products hierarchy (e.g., vaccine products) as well as use of General Concept Inclusion functionality to model disorder and findings concepts means that combined substances concepts are no longer required. Requests for new instances will be rejected.

#### EXCEPTIONS

Combined dried gels, also known as co-dried gels, are registered as a single "substance" (or a Specified Substance) in the IDMP database, rather than two separate substances. Because the structural modification creates a unique chemical entity with different properties than the sum of its parts, regulators treat it as its own unique ingredient.&#x20;

* For example, 380671000087102 |Aluminium hydroxide magnesium carbonate co-dried gel (substance)|

### Genetic engineering process variations

Concepts representing genetic engineering process variations such as Somatropin (epr), Somatropin (rbe), or Somatropin (rmc) are out of scope as SNOMED CT does not generally differentiate substances based on production process.

* Existing instances will be inactivated. Requests for new instances will be rejected.

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Substance" class="button primary">Provide Feedback</a>
