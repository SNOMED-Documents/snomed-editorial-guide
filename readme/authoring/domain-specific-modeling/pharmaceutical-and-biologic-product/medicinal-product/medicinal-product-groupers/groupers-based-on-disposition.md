# Groupers Based on Disposition

## Overview

A high-level grouper concept supports the organization of the medicinal product concepts based on disposition: 766779001 |Medicinal product categorized by disposition (product)|

Disposition is a behaviour that something can exhibit (or participate in) given the appropriate context in which to do this. For example, a person may be "disposed" (or pre-disposed) to fidget in their seat when in a stressful situation such as an interview. For medicinal products, disposition behavior can be thought of as "mechanism of action" of its active ingredient substance(s): the behavior that the active ingredient substance(s) in the product exhibit when used clinically. Disposition (mechanism of action) is distinguishable from therapeutic role, which is context dependent: for example the mechanism of action of timolol is as a beta-adrenoceptor antagonist; this action can be used therapeutically to reduce hypertension when administered in a product given orally or to treat glaucoma when administered in a product intended to be given ophthalmically. Medicinal products can be collected together into groups based on the disposition of their active ingredient substance(s).

Disposition is a characteristic of the active ingredient substance(s) present in the Medicinal Product, therefore disposition grouping concepts are assigned (inferred) by the classifier to medicinal products and to all their child concepts (medicinal product form and clinical drug concepts) although in a browser such as DailyBuild the inferred grouping concepts will be shown on the proximal concept only (the "medicinal product containing" concept).

<figure><img src="../../../../../../.gitbook/assets/Screenshot 2025-10-01 at 8.48.30 AM (1).png" alt=""><figcaption></figcaption></figure>

<p align="center">Figure: Inferred view of Medicinal product showing membership of a disposition grouping (carbonic anydrase inhibitor)</p>

This section applies to grouper concepts representing a **single** disposition; groupers comprised of multiple dispositions are described in [Groupers Based on Multiple Dispositions, Structures](../../../../../../authoring/pharmaceutical-and-biologic-product/174691077.html).

## Modeling

| **Stated parent concept**                                      | `763158003 \|Medicinal product (product)`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Semantic tag**                                               | (product)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Definition status**                                          | Defined                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <p><strong>Attribute:</strong></p><p>Has active ingredient</p> | <p><strong>Range:</strong> <code>&#x3C;&#x3C;105590001 |Substance (substance)</code></p><ul><li>While the allowed range is broader, the |Medicinal product| grouper concepts based on disposition should only use sufficiently defined grouper concepts that are descendants of <code>766739005 |Substance categorized by disposition (substance)|</code> as attribute values.<br></li></ul><p><strong>Cardinality:</strong> 0..*</p><ul><li>While the allowed range is broader, the |Medicinal product| grouper concepts based on disposition should have one and only one |Has active ingredient| attribute.</li></ul> |

## Naming

### FSN

Product containing \<Active ingredient PT> (product)

For example,

* Product containing histamine receptor antagonist (product)
* Product containing histamine H2 receptor antagonist (product)

Align naming and case sensitivity with the PT for the concept that is selected as the 726542003 |Has disposition (attribute)| attribute value for the substance concept used as the attribute value for the 127489000 |Has active ingredient (attribute)|.

### Preferred Term

\<Active ingredient PT>-containing product

For example,

* Histamine receptor antagonist-containing product
* Histamine H2 receptor antagonist-containing product

Align naming and case significance with the PT for the concept that is selected as the 726542003 |Has disposition (attribute)| attribute value for the substance concept used as the attribute value for the 127489000 |Has active ingredient (attribute)|.

### Synonym

Synonyms matching the FSN are not required.

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/image (31) (1) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for grouper concept 6425004 |Product containing histamine receptor antagonist (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (32) (1) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for grouper concept 6425004 |Product containing histamine receptor antagonist (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (33) (1) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for grouper concept 108661002 |Product containing histamine H2 receptor antagonist (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (34) (1) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for grouper concept 108661002 |Product containing histamine H2 receptor antagonist (product)|</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690992.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Groupers%20Based%20on%20Disposition" class="button primary">Provide Feedback</a>
