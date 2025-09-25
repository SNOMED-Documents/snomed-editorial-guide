# Groupers Based on Multiple Dispositions, Structures

## Overview

Groupers comprised of two or more existing disposition and/or structure groupers that can be sufficiently defined may be included in the |Medicinal product| hierarchy. High-level grouper concepts support the organization of the combined groupers based on disposition and/or structure:

* 766779001 |Medicinal product categorized by disposition (product)|
* 763760008 |Medicinal product categorized by structure (product)|

For some medicinal products, their clinical usefulness is related to the combination of both their structure and their disposition; it is the structure that produces the disposition.

For example,

* Clemastine is a substance whose anti-histamine behaviour is based upon its structure being ethanolamine derived.

Since structure-based grouping and disposition are characteristics of the active ingredient substance(s) present in the medicinal product, combined 'structure and disposition grouping' concepts are inferred by the classifier to medicinal products and include all their child concepts (medicinal product form and clinical drug concepts), although in a browser, the inferred grouping concepts are shown on the proximal concept only (the "medicinal product containing" concept).

<figure><img src="https://confluence.ihtsdotools.org/download/attachments/293568803/MP%20with%20Structure%20and%20Disposition%20grouping.png?version=1&#x26;modificationDate=1748543718000&#x26;api=v2" alt="MP with Structure and Disposition grouping.png"><figcaption><p>Figure 1. Medicinal Product showing membership of a structure-and-disposition grouping (ethanolamine derivative and histamine receptor antagonist)</p></figcaption></figure>

## Modeling

| **Stated parent concept**                                                       | 763158003 \|Medicinal product (product)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Semantic tag**                                                                | (product)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Definition status**                                                           | Defined                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <p><strong>Attribute:</strong></p><p><strong>Has active ingredient</strong></p> | <p>Range: &#x3C;&#x3C;105590001 |Substance (substance)</p><ul><li>While the allowed range is broader, the |Medicinal product| combined grouper concepts based on disposition and/or structure should only use sufficiently defined grouper concepts that are descendants of 766739005 |Substance categorized by disposition (substance)| and/or primitive grouper concepts that are descendants of 312413002 |Substance categorized by structure (substance)| as attribute values.</li></ul><p>Cardinality: 0..*</p><ul><li>While the allowed range is broader, the |Medicinal product| combined grouper concepts should have one or more |Has active ingredient| attributes.</li></ul> |

## Naming

### FSN

Use the following pattern for the FSN if the combined grouper is comprised of two dispositions or two structural groupers; align naming and case significance with the PT as described in Section 4.1 and 4.2, respectively. The active ingredients must be in alphabetical order and separated by the word “and”.

* Product containing \<Active ingredient PT> and \<Active ingredient PT> (product)
  * For example,
    * Product containing norepinephrine reuptake inhibitor and serotonin reuptake inhibitor (product)

Use the following pattern for the FSN if the combined grouper is comprised of one disposition and one structural grouper; align naming and case significance with the FSN for the concept with the FSN as described in Section 4.1 and 4.2, respectively.

* Product containing \<Structural grouper active ingredient PT> and \<Disposition grouper active ingredient PT> (product)
  * For example,
    * Product containing piperazine derivative and histamine receptor antagonist (product)

### Preferred Term

Use the following pattern for the FSN if the combined grouper is comprised of two dispositions or two structural groupers; align naming and case significance with the PT as described in Section 4.1 and 4.2, respectively. The active ingredients must be in alphabetical order and separated by the word “and”.

* Product containing \<Active ingredient PT> and \<Active ingredient PT> (product)
  * For example,
    * Product containing norepinephrine reuptake inhibitor and serotonin reuptake inhibitor (product)

Use the following pattern for the FSN if the combined grouper is comprised of one disposition and one structural grouper; align naming and case significance with the FSN for the concept with the FSN as described in Section 4.1 and 4.2, respectively.

* Product containing \<Structural grouper active ingredient PT> and \<Disposition grouper active ingredient PT> (product)
  * For example,
    * Product containing piperazine derivative and histamine receptor antagonist (product)

### Synonym

Synonyms matching the FSN are not required.

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/image (35) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for combined grouper concept 767562003 |Product containing norepinephrine reuptake inhibitor and serotonin reuptake inhibitor (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (36) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for combined grouper concept 767562003 |Product containing norepinephrine reuptake inhibitor and serotonin reuptake inhibitor (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (38) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for combined grouper concept 70343008 |Product containing piperazine derivative and histamine receptor antagonist (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (37) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for combined grouper concept 70343008 |Product containing piperazine derivative and histamine receptor antagonist (product)|</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174691078.png" alt=""><figcaption></figcaption></figure>
