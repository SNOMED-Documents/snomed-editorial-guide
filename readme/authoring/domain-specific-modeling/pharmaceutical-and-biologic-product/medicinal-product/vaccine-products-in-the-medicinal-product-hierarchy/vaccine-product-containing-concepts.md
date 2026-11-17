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

# Vaccine Product containing Concepts

## Overview

The _Vaccine product containing_ concept is an abstract representation of the active ingredient(s) in a vaccine product. It means that the vaccine product must contain the active ingredient(s) specified in the FSN but may also contain a modification of the active ingredient(s) specified in the FSN or may contain additional active ingredient(s).

#### Single ingredient vaccines

Both _Vaccine product containing_ and _Vaccine product containing only_ concepts may be created for products that only have one active ingredient.

* For example,
  * 836374004 |Vaccine product containing Hepatitis B virus antigen (medicinal product)|
  * 871822003 |Vaccine product containing only Hepatitis B virus antigen (medicinal product)|

#### Multiple ingredient vaccines

_Vaccine product containing_ concepts are not created for multiple ingredient vaccine products.

_Vaccine product containing only_ concepts are created for multiple ingredient vaccine products.

## Naming

Microorganism nomenclature changes regularly as taxonomy and classification are revised. These changes influence how antigens are named and how vaccine products are represented. As a result, historical microorganism names may no longer correspond to the current taxonomic structure, even though they remain familiar and clinically accepted.  To ensure vaccine products remain recognisable and consistent with regulatory documentation, the FSN will use the current biological organism name as reflected by the attribute value for the |Has active ingredient (attribute)|, while the PT will retain the established, clinically familiar name used in product information.

For multiple ingredient vaccine products, the active ingredients are listed in alphabetical order, separated by the word _and_, and the word _antigen_ is omitted.

For concepts where all active ingredients are a virus, the word _virus_ may be omitted and added before _antigens_.

### FSN

Template:

* Vaccine product containing \<active ingredient PT> (medicinal product)

For example,

* Vaccine product containing Haemophilus influenzae type b antigen (medicinal product)
* Vaccine product containing Orthoebolavirus antigen (medicinal product)

### Preferred Term

Use the following pattern for the PT; align terming and case significance with the common, clinically recognizable synonym for the concept that is selected as the attribute value for the |Has active ingredient (attribute)|.

Template:

* \<Active ingredient using common name of organism>-containing vaccine product

For example,

* Ebolavirus antigen-containing vaccine product
* Haemophilus influenzae type b antigen-containing product

### Synonym

Synonyms matching the FSN are not required.

Synonyms corresponding to the disorder that is the target of the vaccine are not allowed; they may be applied to the "Vaccine product containing only" concepts.

## Modeling

<table data-header-hidden><thead><tr><th width="265.6484375"></th><th></th></tr></thead><tbody><tr><td>Stated parent concept</td><td>763158003 |Medicinal product (product)</td></tr><tr><td>Semantic tag</td><td>(medicinal product)</td></tr><tr><td>Definition status</td><td>Defined</td></tr><tr><td><p>Attribute:</p><p>Has active ingredient</p></td><td><p><strong>Range:</strong> &#x3C;105590001 |Substance (substance) excluding concepts representing structural groupers, dispositions, or combined substances</p><p><strong>Cardinality</strong>: 1..*</p><ul><li>While the allowed range is broader, "Vaccine product containing" concepts in the International Release should have one and only one |Has active ingredient| attribute.</li></ul><p>For content in the International Release, this attribute value should represent the organism antigen, not a modification or subtype, unless explicitly identified as an exception.</p><p><strong>Exceptions:</strong> Vaccine product containing concepts for the following substance subtypes are included (to support vaccination certificates):</p><ul><li>161000221102 |Antigen of Corynebacterium diphtheriae toxoid (substance)|</li><li>551000221106 |Antigen of Clostridium tetani toxoid (substance)|</li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Plays role</p></td><td><p><strong>Range</strong>: &#x3C;&#x3C;766940004 |Role (role)|<br></p><p><strong>Cardinality</strong>: 0..*</p><ul><li>While the allowed range is broader, "Vaccine product containing" concepts should have one and only one |Plays role| attribute with attribute value = 318331000221102 |Active immunity stimulant therapeutic role (role)|.</li></ul></td></tr></tbody></table>

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/Screenshot 2026-11-12 at 9.38.53 AM.png" alt=""><figcaption><p>Stated view of 836380007 |Vaccine product containing Haemophilus influenzae type b antigen (medicinal product)|</p></figcaption></figure>



<figure><img src="../../../../../../.gitbook/assets/Screenshot 2026-11-12 at 9.42.02 AM.png" alt=""><figcaption><p>Inferred view of 836380007 |Vaccine product containing Haemophilus influenzae type b antigen (medicinal product)|</p></figcaption></figure>

<figure><img src="https://github.com/SNOMED-Documents/snomed-editorial-guide/blob/main/authoring/pharmaceutical-and-biologic-product/images/174690932.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Vaccine%20Product%20containing%20Concepts" class="button primary">Provide Feedback</a>
