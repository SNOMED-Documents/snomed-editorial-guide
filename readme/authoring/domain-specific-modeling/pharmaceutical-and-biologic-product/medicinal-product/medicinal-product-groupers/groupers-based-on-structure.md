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

# Groupers Based on Structure

## Overview

A high-level grouper concept supports the organization of the hierarchy based on structure: 763760008 |Medicinal product categorized by structure (product)|

All substances have spatial arrangement of the atoms and molecules and bonds that they are constituted from and which therefore govern the final shape that the substance takes; this arrangement is their "structure". Substance structures often follow patterns so that similar structures are grouped together and often share particular name patterns. Medicinal products can be collected together into groups based on the structural pattern(s) of their active ingredient substance(s).

Structure-based grouping is a characteristic of the active ingredient substance(s) present in the medicinal product, therefore structure-based grouping concepts are assigned (inferred) by the classifier to medicinal products and include all their child concepts (medicinal product form and clinical drug concepts) although in a browser such as the DailyBuild, the inferred grouping concepts will be shown on the proximal concept only (the "medicinal product containing" concept).

<figure><img src="../../../../../../.gitbook/assets/Screenshot 2025-10-01 at 8.48.30 AM.png" alt=""><figcaption></figcaption></figure>

<p align="center">Inferred view of Medicinal product showing membership of a structural grouping (sulfonamide)</p>

{% hint style="info" %}
This section applies to grouper concepts representing a **single** structure; groupers comprised of multiple structures are described in [Groupers Based on Multiple Dispositions, Structures](https://github.com/SNOMED-Documents/snomed-editorial-guide/blob/main/authoring/pharmaceutical-and-biologic-product/174691077.html).
{% endhint %}

## Naming

### FSN

Product containing \<active ingredient> (product)

Align naming and case sensitivity with the Preferred Term for the concept that is selected as the attribute value for the 127489000 |Has active ingredient (attribute)|.

For example,

* Product containing prostaglandin (product)
* Product containing A series prostaglandin (product)

### Preferred Term

\<Active ingredient>-containing product

Align naming and case significance with the Preferred Term for the concept that is selected as the attribute value.

For example,

* Prostaglandin-containing product
* A series prostaglandin-containing product

### Synonym

Synonyms matching the FSN are not required.

## Modeling

<table data-header-hidden><thead><tr><th width="329.408203125"></th><th></th></tr></thead><tbody><tr><td><strong>Stated parent concept</strong></td><td><code>763158003 |Medicinal product (product)</code></td></tr><tr><td><strong>Semantic tag</strong></td><td>(product)</td></tr><tr><td><strong>Definition status</strong></td><td>Defined</td></tr><tr><td><p><strong>Attribute:</strong></p><p>Has active ingredient</p></td><td><strong>Range:</strong> <code>&#x3C;&#x3C; 105590001</code></td></tr></tbody></table>

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/image (27) (1) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 350067007 |Product containing prostaglandin (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (28) (1) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 350067007 |Product containing prostaglandin (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (29) (1) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 350068002 |Product containing A series prostaglandin (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (30) (1) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 350068002 |Product containing A series prostaglandin (product)|</p></figcaption></figure>

<figure><img src="https://github.com/SNOMED-Documents/snomed-editorial-guide/blob/main/authoring/pharmaceutical-and-biologic-product/images/174691044.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Groupers%20Based%20on%20Structure" class="button primary">Provide Feedback</a>
