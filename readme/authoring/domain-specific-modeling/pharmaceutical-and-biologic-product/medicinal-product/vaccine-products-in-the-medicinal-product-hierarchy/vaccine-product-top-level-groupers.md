# Vaccine Product Top Level Groupers

## Overview

The following high level vaccine-related grouper concepts are included in the |Medicinal product| hierarchy.

* 787859002 |Vaccine product (medicinal product)|
  * 836368004 |Vaccine product containing bacteria antigen (medicinal product)|
  * 1290123005 |Vaccine product containing protozoa antigen (medicinal product)|
  * 836369007 |Vaccine product containing virus antigen (medicinal product)|

## Modeling

<table data-header-hidden><thead><tr><th width="270"></th><th></th></tr></thead><tbody><tr><td><strong>Stated parent concept</strong></td><td>763158003 |Medicinal product (product)</td></tr><tr><td><strong>Semantic tag</strong></td><td>(medicinal product)</td></tr><tr><td><strong>Definition status</strong></td><td>Defined</td></tr><tr><td><p><strong>Attribute:</strong></p><p>Has active ingredient</p></td><td><p>Range: &#x3C;&#x3C;105590001 |Substance (substance)|<br></p><p>Cardinality: 0..*</p><p><em>Exception:  Top level grouper 787859002 |Vaccine product (medicinal product)| does not have a Has active ingredient (attribute).</em></p></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Plays role</p></td><td><p>Range: &#x3C;&#x3C;766940004 |Role (role)|<br></p><p>Cardinality: 0..*</p><ul><li>While the allowed range is broader, top level vaccine-related grouper concepts should have one and only one Plays role (attribute) with attribute value = 318331000221102 |Active immunity stimulant therapeutic role (role)|.</li></ul></td></tr></tbody></table>

## Naming

### FSN

Use the following pattern for the FSN; align naming and case sensitivity with the PT for the concept that is selected as the attribute value for the 127489000 |Has active ingredient (attribute)|.

Vaccine product containing \<Active ingredient PT excluding "antigen"> antigen (medicinal product)

Vaccine product containing \<Active ingredient PT excluding "antigen"> and \<Active ingredient PT excluding "antigen"> antigens (medicinal product)

* For example,
  * Vaccine product (medicinal product)
  * Vaccine product containing bacteria antigen (medicinal product)
  * Vaccine product containing virus antigen (medicinal product)
  * Vaccine product containing bacteria and virus antigens (medicinal product)

### Preferred Term

Use the following pattern for the PT; align naming and case significance with the PT for the concept that is selected as the attribute value for the 127489000 |Has active ingredient (attribute)|.

\<Active ingredient PT excluding "antigen">-containing vaccine product

\<Active ingredient PT excluding "antigen">- and \<Active ingredient PT excluding "antigen"> antigens-containing vaccine product

* For example,
  * Vaccine product
  * Bacteria antigen-containing vaccine product
  * Virus antigen-containing vaccine product
  * Bacteria- and virus antigens-containing vaccine product

### Synonym

Synonyms matching the FSN are not required.

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/image (43) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 787859002 |Vaccine product (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (44) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 787859002 |Vaccine product (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (45) (1).png" alt=""><figcaption><p>S<strong>tated</strong> view for 836368004 |Vaccine product containing bacteria antigen (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (46) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 836368004 |Vaccine product containing bacteria antigen (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (47) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 863950005 |Vaccine product containing bacteria and virus antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (48) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 863950005 |Vaccine product containing bacteria and virus antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690909.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Vaccine%20Product%20Top%20Level%20Groupers" class="button primary">Provide Feedback</a>
