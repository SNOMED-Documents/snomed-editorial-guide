# Vaccine Product Top Level Groupers

## Overview

The following high level vaccine-related grouper concepts are included in the |Medicinal product| hierarchy.

* 787859002 |Vaccine product (medicinal product)|
  * 836368004 |Vaccine product containing bacteria antigen (medicinal product)|
  * 1290123005 |Vaccine product containing protozoa antigen (medicinal product)|
  * 836369007 |Vaccine product containing virus antigen (medicinal product)|

## Modeling

| **Stated parent concept**                                                       | 763158003 \|Medicinal product (product)                                                                                                                                                                                                                                                                                   |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Semantic tag**                                                                | (medicinal product)                                                                                                                                                                                                                                                                                                       |
| **Definition status**                                                           | Defined                                                                                                                                                                                                                                                                                                                   |
| <p><strong>Attribute:</strong></p><p><strong>Has active ingredient</strong></p> | <p>Range: &#x3C;&#x3C;105590001 |Substance (substance)|</p><p>Cardinality: 0..*</p><p><em>Exception:  Top level grouper 787859002 |Vaccine product (medicinal product)| does not have a Has active ingredient (attribute).</em></p>                                                                                       |
| <p><strong>Attribute:</strong></p><p><strong>Plays role</strong></p>            | <p>Range: &#x3C;&#x3C;766940004 |Role (role)|</p><p>Cardinality: 0..*</p><ul><li>While the allowed range is broader, top level vaccine-related grouper concepts should have one and only one Plays role (attribute) with attribute value = 318331000221102 |Active immunity stimulant therapeutic role (role)|.</li></ul> |

## Terming

### FSN

Use the following pattern for the FSN; align naming and case sensitivity with the PT for the concept that is selected as the attribute value for the 127489000 |Has active ingredient (attribute)|.

Vaccine product containing \<Active ingredient PT excluding "antigen"> antigen (medicinal product)

Vaccine product containing \<Active ingredient PT excluding "antigen"> and \<Active ingredient PT excluding "antigen"> antigens (medicinal product)

For example,

* Vaccine product (medicinal product)
* Vaccine product containing bacteria antigen (medicinal product)
* Vaccine product containing virus antigen (medicinal product)
* Vaccine product containing bacteria and virus antigens (medicinal product)

### Preferred Term

Use the following pattern for the PT; align naming and case significance with the PT for the concept that is selected as the attribute value for the 127489000 |Has active ingredient (attribute)|.

\<Active ingredient PT excluding "antigen">-containing vaccine product

\<Active ingredient PT excluding "antigen">- and \<Active ingredient PT excluding "antigen"> antigens-containing vaccine product

For example,

* Vaccine product
* Bacteria antigen-containing vaccine product
* Virus antigen-containing vaccine product
* Bacteria- and virus antigens-containing vaccine product

### Synonym

Synonyms matching the FSN are not required.

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/image (43).png" alt=""><figcaption><p><strong>Stated</strong> view for 787859002 |Vaccine product (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (44).png" alt=""><figcaption><p><strong>Inferred</strong> view for 787859002 |Vaccine product (product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (45).png" alt=""><figcaption><p>S<strong>tated</strong> view for 836368004 |Vaccine product containing bacteria antigen (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (46).png" alt=""><figcaption><p><strong>Inferred</strong> view for 836368004 |Vaccine product containing bacteria antigen (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (47).png" alt=""><figcaption><p><strong>Stated</strong> view for 863950005 |Vaccine product containing bacteria and virus antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (48).png" alt=""><figcaption><p><strong>Inferred</strong> view for 863950005 |Vaccine product containing bacteria and virus antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690909.png" alt=""><figcaption></figcaption></figure>
