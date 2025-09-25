# Conjugate acids, bases and salts

## Overview

Acids substance concepts should be modeled with a structural parent concept.

Salts should be modeled with a conjugate base as parent (if one exists, otherwise they are modeled with a structural parent). Salts may have an Is modification of (attribute) relationship to the conjugate acid where a specific use case is identified. See examples of such use cases at [Concepts Representing a Substance or its Modifications](../guidelines-for-substance-hierarchy-grouper-concepts/concepts-representing-a-substance-or-its-modifications.md).

Conjugate base concepts (e.g., valproate, pamidronate, etidronate) should only be created where a specific use case is identified, for example, when required to support the definition of other concepts in the terminology.

Conjugate bases should be created as separate concepts - not added as synonyms to the corresponding acid concept.

New instances of substance concepts containing the word _salt_ will not be added. The existing concepts will be reviewed, and if possible, will be replaced by equivalent compounds.

## Modeling

<table data-header-hidden><thead><tr><th width="231.39453125">Parent concept</th><th>Most distal appropriate descendant of 312413002 |Substance categorized structurally (substance)|</th></tr></thead><tbody><tr><td><strong>Parent concept</strong></td><td>Most distal appropriate descendant of 312413002 |Substance categorized structurally (substance)|</td></tr><tr><td><strong>Semantic tag</strong></td><td>(substance)</td></tr><tr><td><strong>Definition status</strong></td><td>Primitive</td></tr><tr><td><p><strong>Attribute:</strong> </p><p><strong>Is Modification of</strong></p></td><td><p>Range  &#x3C;105590001 |Substance (substance)|</p><p>Cardinality: 0..1</p><p>Used to identify the conjugate acid</p></td></tr><tr><td><p><strong>Attribute:</strong> </p><p><strong>Has disposition</strong></p></td><td><p>Range:  &#x3C;726711005 |Disposition (disposition)|</p><ul><li>While the allowed range is broader, substance concepts should only use &#x3C;726711005 |Disposition (disposition)| as the attribute value.</li></ul><p>Cardinality: 0..1</p></td></tr></tbody></table>

## Naming

Where INN names exist, these should be used for the FSN and PT.

### FSN

Pattern:

* X sulfate (substance)
* X pamidronate (substance)

For example,

* Copper sulfate (substance)
* **Disodium pamidronate (substance)**
* Etidronate (substance)

Exception:

* Valproate sodium (substance)

***

### Preferred Term

Pattern:

* X sulfate
* X pamidronate

For example,

* Copper sulfate
* Pamidronate monosodium
* Etidronate

Exception:

* Valproate sodium

***

### Synonyms

Pattern: Pamidronate X

For example,

* Pamidronate monosodium
* Valproate sodium

## Exemplar

Stated view of 387080000 |Valproic acid (substance)|:

<figure><img src="../../../../../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

Stated and inferred view of 387481005 |Sodium valproate (substance)|:

<figure><img src="../../../../../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

Hierarchy view of 264325000 |Valproate (substance)| subtypes:

<figure><img src="../../../../../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **stated** and **inferred** views.

<div align="left"><figure><img src="../../../../../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../../../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure></div>

<figure><img src="../../../../../../authoring/substance/images/174691578.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../../authoring/substance/images/174691579.png" alt=""><figcaption></figcaption></figure>

