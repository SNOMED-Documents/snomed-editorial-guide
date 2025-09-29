# Medicinal Product containing only

## Overview

The |Product containing only x (medicinal product)| concepts are abstract representations of the active ingredient(s) for a medicinal product. The medicinal product contains only the active ingredient(s) specified in the FSN but may also contain a modification of the active ingredient(s) specified in the FSN.

* For example,
  * Product containing only axitinib (medicinal product)
  * Product containing only abacavir and lamivudine (medicinal product)

This is effectively the "set of active moiety(ies)" of the medicinal product. For example, "Product containing amoxicillin only" represents products that must contain _only_ amoxicillin\*\*\*\*((with any type of modification, be it amoxicillin sodium or amoxicillin trihydrate, or no modification, as in amoxicillin (base)); they must _not_ contain any other active ingredients, such as clavulanic acid. This is the closed world view.

### Use case(s) supported by _Medicinal Product containing only_

There are several use cases that the _Medicinal Product containing only_ concept can support:

* In national extensions; where it is useful for various clinical purposes, such as prescribing scenarios (so called "abstract" or "non-product-based" prescribing) and in medication history and in medication profiles
* Internationally and nationally in decision support and in protocols and treatment guidelines
* Internationally and nationally for interoperability of patient medication information such as in patient summaries
* Internationally and nationally for recording adverse events and/or sensitivities to medication, particularly for multi-ingredient preparations where there will be no appropriate single substance concept and it is not possible to say which particular active ingredient is responsible for the issue
* In pharmacovigilance, especially for description of concomitant medications where less information may be available (see below in _IDMP Compatibility_)
* In analysis and research
* As a supporting attribute for other concepts elsewhere in SNOMED CT

### IDMP Compatibility

The _Medicinal Product containing only_ concept might be directly compatible with the ISO 11616 concept of a level 1 Pharmaceutical Product (PhPID\_SUB\_L1), where the "active substance set" comprises the definition of this concept. However, the granularity of description of substance for the PhP1 is not completely clear, but may be more granular than that used for the _Medicinal Product containing only_ concept. The _Medicinal Product containing only_ concept is defined by "only and exclusively the active ingredient substance(s) that it contains but regardless of any modification of those active ingredient substance(s)" whereas the PhP1 will likely use a substance description that includes any modification, including when there are multiple modifications (e.g., a solvated salt modification).

In IDMP, for products using adjuvants, it is probable that the adjuvant would be included as part of the "active substance set" and its role explicitly identified. For example, aluminium hydroxide is used as an adjuvant in several vaccine products (e.g., hepatitis A, hepatitis B) in addition to the antigen itself to enhance the immune response; it is not an active ingredient per se, and it is not an inactive ingredient; it is explicitly an "adjuvant". However, this type of detail of the implementation of the abstract model of ISO 11616 remains unclear, and in its first implementation, the modeling of adjuvants in the vaccine content in the SNOMED CT international edition has not been finalised.

## Modeling

| **Stated parent**                                                    | 763158003 \|Medicinal product (product)        |
| -------------------------------------------------------------------- | ---------------------------------------------- |
| **Semantic tag**                                                     | (medicinal product)                            |
| **Definition status**                                                | Defined                                        |
| <p><strong>Attribute:</strong></p><p><strong>127489000</strong></p>  | Has active ingredient (attribute)              |
| <p><strong>Attribute:</strong></p><p><strong>1142139005</strong></p> | Count of base of active ingredient (attribute) |

#### Exception for Benzylpenicillin

774826003 |Product containing only benzylpenicillin (medicinal product)| is primitive and is a proximal primitive parent to 786119008 |Product containing only benzylpenicillin in oral dose form (medicinal product form)| plus 2 subtype clinical drugs, and 778490002 |Product containing only benzylpenicillin in parenteral dose form (medicinal product form)| plus 3 subtype clinical drugs. 774826003 |Product containing only benzylpenicillin (medicinal product)| is intentionally not modeled as a supertype of 1234764000 |Product containing only benzathine benzylpenicillin (medicinal product)| and 1234762001 |Product containing only procaine benzylpenicillin (medicinal product)| because clinically the child concepts are not considered as specialisations of the supertype, but as sibling concepts.

## Naming

Use the following pattern for the FSN and PT. Align naming and case sensitivity with the FSN for the concept that is selected as the attribute value.

For multiple ingredient drug products, the active ingredients must be in alphabetical order and separated by the word “and”.

### FSN

Product containing only \<Active ingredient FSN> (medicinal product)

Product containing only \<Active ingredient FSN> and \<Active ingredient FSN> (medicinal product)

Product containing only \<Active ingredient FSN> and \<Active ingredient FSN> and \<Active ingredient FSN> (medicinal product)

For example,

* Product containing only axitinib (medicinal product)
* Product containing only abacavir and lamivudine (medicinal product)
* Product containing only abacavir and lamivudine and zidovudine (medicinal product)

### Preferred Term

\<Active ingredient PT> only product

\<Active ingredient PT> and \<Active ingredient PT> only product

\<Active ingredient PT> and \<Active ingredient PT> and \<Active ingredient PT> only product

For example,

* Axitinib only product
* Abacavir and lamivudine only product
* Abacavir and lamivudine and zidovudine only product

### Synonym

Synonyms matching the FSN are not required.

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/image (50) (1).png" alt=""><figcaption><p>Stated Template View</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (51) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 773390003 |Product containing only axitinib (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (52) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 773390003 |Product containing only axitinib (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (84).png" alt=""><figcaption><p><strong>Stated</strong> view for 775360007 |Product containing only codeine and paracetamol (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (85).png" alt=""><figcaption><p><strong>Inferred</strong> view for 775360007 |Product containing only codeine and paracetamol (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/240453150.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Medicinal%20Product%20containing%20only" class="button primary">Provide Feedback</a>
