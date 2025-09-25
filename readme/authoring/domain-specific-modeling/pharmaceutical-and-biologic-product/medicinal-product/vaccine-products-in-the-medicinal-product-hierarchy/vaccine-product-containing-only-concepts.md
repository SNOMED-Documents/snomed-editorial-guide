# Vaccine Product containing only Concepts

## Overview

The Vaccine Product "only" concept is an abstract representation of the active ingredient(s) in a vaccine product. It means that the vaccine product must contain only the active ingredient(s) specified in the FSN but may also contain a modification of the active ingredient(s) specified in the FSN. The vaccine product "containing only" may be sufficient to serve as an interoperability layer or to support prescribing use cases.

For example,

* |Vaccine product containing only Hepatitis B virus antigen (medicinal product)|
  * |Vaccine product containing only Vaccinia virus antigen (medicinal product)|
  * |Vaccine product containing only Hepatitis A and Hepatitis B virus antigens (medicinal product)|
  * |Vaccine product containing only Bordetella pertussis and Clostridium tetani and Corynebacterium diphtheriae antigens (medicinal product)|

Both vaccine product "containing" and vaccine product "containing only" concepts may be created for products that only have one active ingredient (e.g. 836374004 |Vaccine product containing Hepatitis B virus antigen (medicinal product)| and 871822003 |Vaccine product containing only Hepatitis B virus antigen (medicinal product)|). Vaccine product "containing" concepts are not created for multiple ingredient vaccine products; vaccine product "containing only" concepts are created for multiple ingredient vaccine products.

Modeling and terming for vaccines that have variable composition (e.g. influenza that may be specific to a year or hemisphere) will be addressed at a future date when use cases and requirements are better understood.

## Modeling

| **Stated parent concept**                                                                    | 763158003 \|Medicinal product (product)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Semantic tag**                                                                             | (medicinal product)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Definition status**                                                                        | Defined                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <p><strong>Attribute:</strong></p><p><strong>Has active ingredient</strong></p>              | <p>Range: &#x3C;105590001 |Substance (substance)| excluding concepts representing structural groupers, dispositions, or combined substances</p><p>Cardinality: 1..*</p><ul><li>There is no technical limit on the number of Has active ingredient attributes that may be added to a concept; a practical limit may be imposed at a later date.</li></ul><p>For content in the International Release, this attribute value should represent either the organism antigen, or the organism antigen(s), including modifications or subtypes, that are contained in a manufactured product.</p> |
| **Attribute: Has ingredient qualitative strength**                                           | <p>Range: &#x3C; 1149484003 |Ingredient qualitative strength (qualifier value)|</p><p>Cardinality: 0..*</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Attribute: Has target population**                                                         | <p>Range: &#x3C; 27821000087106 |Product target population (qualifier value)|</p><p>Cardinality: 0..1</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <p><strong>Attribute:</strong></p><p><strong>Plays role</strong></p>                         | <p>Range:  &#x3C;&#x3C;766940004 |Role (role)|</p><p>Cardinality: 0..*</p><ul><li>While the allowed range is broader, Vaccine product "containing" concepts should have one and only one |Plays role (attribute)| of 318331000221102 |Active immunity stimulant role (role)|.</li></ul>                                                                                                                                                                                                                                                                                                    |
| <p><strong>Attribute:</strong></p><p><strong>Count of base of active ingredient</strong></p> | <p>Range: &#x3C; 260299005 |Number (qualifier value)|</p><p>Cardinality: 1..1</p><p>For content in the International Release, this attribute value should represent the total number of discrete active ingredients, excluding modifications or subtypes.</p>                                                                                                                                                                                                                                                                                                                              |
| <p><strong>Attribute:</strong></p><p><strong>Count of active ingredient</strong></p>         | <p>Concrete Type:  Integer<br>Range:  >#0..<br>Cardinality:  1..1</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |

## Terming

### FSN

Use the following pattern for the FSN; align terming and case sensitivity with the PT for the concept that is selected as the attribute value for the |Has active ingredient (attribute)|. For multiple ingredient vaccine products, the active ingredients must be listed in alphabetical order, separated by the word "and", and the word "antigen" will be omitted. For concepts where all active ingredients are virus, the word "virus" may be omitted and added before "antigens".

* Vaccine product containing only \<Active ingredient PT> (medicinal product)
* Vaccine product containing only \<Active ingredient PT> and \<Active ingredient PT> antigens (medicinal product)
* Vaccine product containing only \<Active ingredient PT> and \<Active ingredient PT> and \<Active ingredient PT> antigens (medicinal product)

For example,

* Vaccine product containing only Hepatitis B virus antigen (medicinal product)
* Vaccine product containing only Hepatitis A and Hepatitis B virus antigens (medicinal product)
* Vaccine product containing only Bordetella pertussis and Clostridium tetani and Corynebacterium diphtheriae antigens (medicinal product)\
  \


|Has product characteristic| and |Has ingredient characteristic| attribute values should be added as appropriate.

* Example of |Has product characteristic (attribute)|:
  * Adult vaccine product containing only Hepatitis A virus antigen (medicinal product)
  * Pediatric vaccine product containing only Hepatitis A virus antigen (medicinal product)
  * Adult vaccine product containing only acellular Bordetella pertussis and Clostridium tetani toxoid and Corynebacterium diphtheriae toxoid antigens (medicinal product)
* Example of |Has ingredient characteristic (attribute):
  * Vaccine product containing only Clostridium tetani and low dose Corynebacterium diphtheriae antigens (medicinal product)
  * Vaccine product containing only Clostridium tetani and low dose Corynebacterium diphtheriae and inactivated Human poliovirus antigens (medicinal product)

### Preferred Term

Use the following pattern for the PT; align terming and case significance with the PT for the concept that is selected as the attribute value for the |Has active ingredient (attribute)|. For multiple ingredient vaccine products, the active ingredients must be listed in alphabetical order, separated by the word "and", and the word "antigen" will be omitted. For concepts where all active ingredients are virus, the word "virus" may be omitted and added before "antigens".

* \<Active ingredient PT> only vaccine product
* \<Active ingredient PT> and \<Active ingredient PT> antigen only vaccine product
* \<Active ingredient PT> and \<Active ingredient PT> and \<Active ingredient PT> antigen only vaccine product
* For example,
  * Hepatitis B virus antigen only vaccine product
  * Hepatitis A and Hepatitis B virus antigens only vaccine product
  * Bordetella pertussis and Clostridium tetani and Corynebacterium diphtheriae antigens only vaccine product

|Has product characteristic| and |Has ingredient characteristic| attribute values should be added as appropriate.

* Example of |Has product characteristic (attribute)|:
  * Hepatitis A virus antigen only adult vaccine product
  * Hepatitis A virus antigen only pediatric vaccine product
  * Adult acellular Bordetella pertussis and Clostridium tetani toxoid and Corynebacterium diphtheriae toxoid antigens only vaccine product
* Example of |Has ingredient characteristic (attribute):
  * Clostridium tetani and low dose Corynebacterium diphtheriae antigens only vaccine product
  * Clostridium tetani and low dose Corynebacterium diphtheriae and inactivated Human poliovirus antigens only vaccine product

### Synonym

Synonyms matching the FSN are not required.

Synonyms corresponding to the disorder that is the target of the vaccine are allowed. For multiple ingredient vaccine products, the disorders must be listed in alphabetical order and separated by the word "and". Note that these are not true synonyms; they may be updated and identified as "near-synonym" descriptions when that functionality becomes available.

For example,

* Hepatitis B vaccine
* Hepatitis A and Hepatitis B vaccine
* Diphtheria and pertussis and tetanus vaccine

|Has product characteristic| and |Has ingredient characteristic| attribute values should be added as appropriate.

* Example of |Has product characteristic (attribute)|:
  * Hepatitis A adult vaccine
  * Hepatitis A pediatric vaccine
  * Diphtheria toxoid and acellular pertussis and tetanus toxoid adult vaccine
* Example of |Has ingredient characteristic (attribute):
  * Low dose diphtheria and tetanus vaccine
  * Low dose diphtheria and inactivated poliomyelitis and tetanus vaccine

Synonyms representing abbreviations for product (e.g. MMR, DTaP) will not be included in the International Release due to lack of internationally accepted reference source.

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/image (62).png" alt=""><figcaption><p><strong>Stated</strong> view for 871822003 |Vaccine product containing only Hepatitis B virus antigen (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (63).png" alt=""><figcaption><p> <strong>Inferred</strong> view for 871822003 |Vaccine product containing only Hepatitis B virus antigen (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (64).png" alt=""><figcaption><p><strong>Stated</strong> view for 871803007 |Vaccine product containing only Hepatitis A and Hepatitis B virus antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (66).png" alt=""><figcaption><p><strong>Inferred</strong> view for 871803007 |Vaccine product containing only Hepatitis A and Hepatitis B virus antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (65).png" alt=""><figcaption><p><strong>Stated</strong> view for 1991000221106 |Vaccine product containing only Human papillomavirus 16 and 18 antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (67).png" alt=""><figcaption><p><strong>Inferred</strong> view for 1991000221106 |Vaccine product containing only Human papillomavirus 16 and 18 antigens (medicinal product)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (68).png" alt=""><figcaption><p><strong>Stated</strong> view for 865997008 |Adult vaccine product containing only Hepatitis A virus antigen (medicinal product)| and illustrates the use of the "Has product characteristic" attribute</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (69).png" alt=""><figcaption><p><strong>Inferred</strong> view for 865997008 |Adult vaccine product containing only Hepatitis A virus antigen (medicinal product)| and illustrates the use of the "Has product characteristic" attribute</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (70).png" alt=""><figcaption><p><strong>Stated</strong> view for 871838009 |Vaccine product containing only Clostridium tetani and low dose Corynebacterium diphtheriae and inactivated Human poliovirus antigens (medicinal product)| and illustrates use of the "Has ingredient characteristic" attribute</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (71).png" alt=""><figcaption><p><strong>Inferred</strong> view for 871838009 |Vaccine product containing only Clostridium tetani and low dose Corynebacterium diphtheriae and inactivated Human poliovirus antigens (medicinal product)| and illustrates use of the "Has ingredient characteristic" attribute</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690945.png" alt=""><figcaption></figcaption></figure>






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=SCT+Editorial+Guide&entry.670899847=Vaccine%20Product%20containing%20only%20Concepts" class="button primary">Provide Feedback</a>
