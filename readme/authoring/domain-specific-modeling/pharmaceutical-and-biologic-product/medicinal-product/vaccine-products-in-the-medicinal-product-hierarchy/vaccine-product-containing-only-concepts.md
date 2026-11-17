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

# Vaccine Product containing only Concepts

## Overview

The _Vaccine product containing only_ concept is an abstract representation of the active ingredient(s) in a vaccine product. It means that the vaccine product must contain only the active ingredient(s) specified in the FSN but may also contain a modification of the active ingredient(s) specified in the FSN. The _Vaccine product containing only_ may be sufficient to serve as an interoperability layer or to support prescribing use cases.

#### Single ingredient vaccines

Both _Vaccine product containing_ and _Vaccine product containing only_ concepts may be created for products that only have one active ingredient.

* For example,
  * 836374004 |Vaccine product containing Hepatitis B virus antigen (medicinal product)| and 871822003 |Vaccine product containing only Hepatitis B virus antigen (medicinal product)|

#### Multiple ingredient vaccines

_Vaccine product containing_ concepts are not created for multiple ingredient vaccine products. _Vaccine product containing only_ concepts are created for multiple ingredient vaccine products.

{% hint style="info" %}
Modeling and terming for vaccines that have variable composition (e.g., influenza specific to a year or hemisphere) will be addressed at a future date when use cases and requirements are better understood.
{% endhint %}

## Naming

Microorganism nomenclature changes regularly as taxonomy and classification are revised. These changes influence how antigens are named and how vaccine products are represented. As a result, historical microorganism names may no longer correspond to the current taxonomic structure, even though they remain familiar and clinically accepted.  To ensure vaccine products remain recognisable and consistent with regulatory documentation, the FSN will use the current biological organism name as reflected by the attribute value for the |Has active ingredient (attribute)|, while the PT will retain the established, clinically familiar name used in product information.

For multiple ingredient vaccine products, the active ingredients are listed in alphabetical order, separated by the word _and_, and the word _antigen_ is omitted.

For concepts where all active ingredients are viruses, the word _virus_ may be omitted and added before "antigens".

### FSN

Template:

* Vaccine product containing only \<active ingredient PT> (medicinal product)
* Vaccine product containing only \<active ingredient PT> and \<active ingredient PT> antigens (medicinal product)
* Vaccine product containing only \<active ingredient PT> and \<active ingredient PT> and \<active ingredient PT> antigens (medicinal product)

For example,

* Vaccine product containing only Orthoebolavirus antigen (medicinal product)
* Vaccine product containing only Clostridium tetani and Corynebacterium diphtheriae antigens (medicinal product)
* Vaccine product containing only Bordetella pertussis and Clostridium tetani and Corynebacterium diphtheriae antigens (medicinal product)

### Preferred Term

Use the following pattern for the PT; align terming and case significance with the common, clinically recognizable synonym for the concept that is selected as the attribute value for the |Has active ingredient (attribute)|.

Template:

* \<Active ingredient using common name of organism> only vaccine product
* \<Active ingredient using common name of organism> and \<active ingredient using common name of organism> antigens only vaccine product
* \<Active ingredient using common name of organism> and \<active ingredient using common name of organism> and \<active ingredient using common name of organism> antigens only vaccine product

For example,

* Ebolavirus antigen only vaccine product
* Clostridium tetani and Corynebacterium diphtheriae antigens only vaccine product
* Bordetella pertussis and Clostridium tetani and Corynebacterium diphtheriae antigens only vaccine product

### Synonym

Synonyms matching the FSN are not required.

Synonyms corresponding to the disorder that is the target of the vaccine are allowed.

For multiple ingredient vaccine products, the disorders must be listed in alphabetical order and separated by the word _and_. Note that these are not true synonyms; they may be updated and identified as near-synonym descriptions when that functionality becomes available.

For example,

* Hepatitis B vaccine
* Hepatitis A and Hepatitis B vaccine
* Diphtheria and pertussis and tetanus vaccine

Synonyms representing abbreviations for product (e.g., MMR, DTaP) will not be included in the International Release due to lack of internationally accepted reference sources.

## Modeling

<table data-header-hidden><thead><tr><th width="280.77734375"></th><th></th></tr></thead><tbody><tr><td><strong>Stated parent concept</strong></td><td>763158003 |Medicinal product (product)</td></tr><tr><td><strong>Semantic tag</strong></td><td>(medicinal product)</td></tr><tr><td><strong>Definition status</strong></td><td>Defined</td></tr><tr><td><p><strong>Attribute</strong>:</p><p>Has active ingredient</p></td><td><p><strong>Range</strong>: &#x3C;105590001 |Substance (substance)| excluding concepts representing structural groupers, dispositions, or combined substances</p><p></p><p><strong>Cardinality</strong>: 1..*</p><ul><li>There is no technical limit on the number of Has active ingredient attributes that may be added to a concept; a practical limit may be imposed at a later date.</li></ul><p>For content in the International Release, this attribute value should represent either the organism antigen, or the organism antigen(s), including modifications or subtypes, that are contained in a manufactured product.</p></td></tr><tr><td><strong>Attribute</strong>:<br>Has ingredient qualitative strength</td><td><p><strong>Range</strong>: &#x3C; 1149484003 |Ingredient qualitative strength (qualifier value)|</p><p></p><p><strong>Cardinality</strong>: 0..*</p></td></tr><tr><td><strong>Attribute</strong>:<br>Has target population</td><td><p><strong>Range</strong>: &#x3C; 27821000087106 |Product target population (qualifier value)|</p><p></p><p><strong>Cardinality</strong>: 0..1</p></td></tr><tr><td><p><strong>Attribute</strong>:</p><p>Plays role</p></td><td><p><strong>Range</strong>: &#x3C;&#x3C;766940004 |Role (role)|<br></p><p><strong>Cardinality</strong>: 0..*</p><ul><li>While the allowed range is broader, "Vaccine product containing" concepts should have one and only one |Plays role (attribute)| of 318331000221102 |Active immunity stimulant role (role)|.</li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Count of base of active ingredient</p></td><td><p><strong>Concrete Type</strong>: Integer</p><p></p><p><strong>Range</strong>: >#0..</p><p></p><p><strong>Cardinality</strong>: 1..1</p><p>For content in the International Release, this attribute value should represent the total number of discrete active ingredients, excluding modifications or subtypes.</p></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Count of active ingredient</p></td><td><p><strong>Concrete Type</strong>: Integer<br></p><p><strong>Range</strong>: >#0..<br></p><p><strong>Cardinality</strong>: 0..1</p></td></tr></tbody></table>

In the pharmaceutical and biologic product model, [ingredient count attributes](https://docs.snomed.org/snomed-ct-specifications/snomed-ct-editorial-guide/readme/authoring/domain-specific-modeling/pharmaceutical-and-biologic-product/pharmaceutical-and-biologic-product-and-dose-form-attributes-summary/ingredient-count-attributes), such as Count of base of active ingredient and Count of active ingredient, are designed under a closed-world assumption solely to ensure accurate subsumption and prevent unexpected subtype classification.  These attributes do not necessarily reflect the strict biological or taxonomic relationships of the underlying antigens or organisms.  They prevent multi-antigen products or products containing multiple subtypes/modifications from incorrectly subsuming under single-antigen or single-base concepts.

{% hint style="warning" %}
The |Count of base of active ingredient (attribute)| and the |Count of active ingredient attribute)| (if applicable) may not necessarily equal the number of |Has active ingredient| attribute-value pairs.
{% endhint %}

Additional count attributes (such as Count of active ingredient) should only be added if omitting them would cause incorrect classification. If removing a count attribute does not alter the intended subsumption hierarchy, it is considered unnecessary.

Where multiple specific subtypes or modifications share the same base category, setting the Count of base of active ingredient to 1 allows proper classification under broader grouper concepts. The specific count of subtypes can optionally be represented using |Count of base and modification pair (attribute)|.

## Exemplars

#### Single ingredient

<figure><img src="../../../../../../.gitbook/assets/Screenshot 2026-11-12 at 9.49.13 AM.png" alt=""><figcaption><p>Stated view of 871764007 |Vaccine product containing only Haemophilus influenzae type b antigen (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/Screenshot 2026-11-12 at 9.50.27 AM.png" alt=""><figcaption><p>Inferred view of 871764007 |Vaccine product containing only Haemophilus influenzae type b antigen (medicinal product)|</p></figcaption></figure>



#### Multiple ingredients

<figure><img src="../../../../../../.gitbook/assets/Screenshot 2026-11-12 at 9.58.10 AM.png" alt=""><figcaption><p>Stated view of 871826000 |Vaccine product containing only Clostridium tetani and Corynebacterium diphtheriae antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/Screenshot 2026-11-12 at 9.59.18 AM.png" alt=""><figcaption><p>Inferred view of 871826000 |Vaccine product containing only Clostridium tetani and Corynebacterium diphtheriae antigens (medicinal product)|</p></figcaption></figure>



#### Two ingredients with same base

<figure><img src="../../../../../../.gitbook/assets/image (65).png" alt=""><figcaption><p><strong>Stated</strong> view for 1991000221106 |Vaccine product containing only Human papillomavirus 16 and 18 antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (67).png" alt=""><figcaption><p><strong>Inferred</strong> view for 1991000221106 |Vaccine product containing only Human papillomavirus 16 and 18 antigens (medicinal product)|</p></figcaption></figure>



#### Vaccine product using |Has target population (attribute)|

<figure><img src="../../../../../../.gitbook/assets/image (68).png" alt=""><figcaption><p><strong>Stated</strong> view for 865997008 |Adult vaccine product containing only Hepatitis A virus antigen (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (69).png" alt=""><figcaption><p><strong>Inferred</strong> view for 865997008 |Adult vaccine product containing only Hepatitis A virus antigen (medicinal product)|</p></figcaption></figure>



#### Vaccine product using |Has ingredient qualitative strength (attribute)|

<figure><img src="../../../../../../.gitbook/assets/image (70).png" alt=""><figcaption><p><strong>Stated</strong> view for 871838009 |Vaccine product containing only Clostridium tetani and low dose Corynebacterium diphtheriae and inactivated Human poliovirus antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (71).png" alt=""><figcaption><p><strong>Inferred</strong> view for 871838009 |Vaccine product containing only Clostridium tetani and low dose Corynebacterium diphtheriae and inactivated Human poliovirus antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="https://github.com/SNOMED-Documents/snomed-editorial-guide/blob/main/authoring/pharmaceutical-and-biologic-product/images/174690945.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Vaccine%20Product%20containing%20only%20Concepts" class="button primary">Provide Feedback</a>
