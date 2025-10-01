# Medicinal Product Form containing

## Overview

The `|Product containing x in y dose form (medicinal product form)|` concept is an abstract representation of active ingredient(s) and dose form intended site for a medicinal product. The medicinal product must contain the active ingredient(s) specified in the FSN but may also contain a modification of the active ingredient(s) specified in the FSN or may contain additional active ingredient(s) as well.

For example,

* Product containing axitinib in oral dose form (medicinal product form)
* Product containing abacavir and lamivudine in oral dose form (medicinal product form)

In other words, "MPF containing" represents a medicinal product based on description of active ingredient substances it contains and on the (generalised) intended site of use for the product.

For example,

* "Product containing amoxicillin in oral dosage form" represents the group of products that must contain some amoxicillin (be it amoxicillin sodium or amoxicillin trihydrate or amoxicillin base), but \_may also\_ contain other active ingredients, such as clavulanic acid, in manufactured dose forms such as oral suspension, oral capsule (any type), oral tablet (any type).

### Use case(s) supported by |Product containing x in y dose form (medicinal product form)|

The main use case for the _MPF (containing)_ is for analysis;, as an aggregation concept for use in research.

### IDMP Compatibility

A concept at this level with the open world view does not correspond to any concept currently in the IDMP suite of standards.

## Modeling

| **Stated parent**                                                   | `763158003 \|Medicinal product (product)`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Semantic tag**                                                    | (medicinal product form)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| _**Definition status**_                                             | Defined                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <p><strong>Attribute:</strong></p><p>Has active ingredient</p>      | <p><strong>Range:</strong> <code>&#x3C;105590001 |Substance (substance)|</code>, excluding concepts representing structural groupers, dispositions, or roles</p><p></p><p><strong>Cardinality:</strong> 1..*</p><p>There is no technical limit on the number of Has active ingredient attributes that may be added to a concept; a practical limit may be imposed at a later date.</p><p></p><p><strong>This attribute is grouped.</strong> </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p><strong>Attribute:</strong></p><p>Has manufactured dose form</p> | <p><strong>Range:</strong> <code>&#x3C;736542009 |Pharmaceutical dose form (dose form)</code></p><ul><li>Only descendants that are groupers representing intended site only (e.g. <code>385268001 |Oral dose form (dose form)|</code>, <code>385287007 |Parenteral dose form (dose form)|</code>)</li></ul><p></p><p><strong>Cardinality:</strong> 1..1</p><p></p><p><strong>Exceptions:</strong> </p><ul><li><code>385217004 |Conventional release gas for inhalation (dose form)|</code> may be used as manufactured dose form for Medicinal product form concepts.</li><li><code>785898006 |Conventional release solution for irrigation (dose form)|</code> does not have <code>736474004 |Has dose form intended site (attribute)|</code> but can be used as a target for manufactured dose form for Medicinal product form concepts.</li></ul><p><strong>Notes</strong></p><ul><li>This attribute describes a grouping dose form concept for the medicinal product, where the grouping is the intended site for administration of the dose form of the product</li></ul> |

## Naming

Use the following pattern for the FSN and PT. Align naming and case sensitivity with the FSN for the concepts that are selected as the attribute value.

For multiple ingredient drug products, active ingredients must be in alphabetical order and separated by the word “and”.

### FSN

Product containing \<Active ingredient FSN> in \<Manufactured dose form FSN> (medicinal product form)

Product containing \<Active ingredient FSN> and \<Active ingredient FSN> in \<Manufactured dose form FSN> (medicinal product form)

Product containing \<Active ingredient FSN> and \<Active ingredient FSN> and \<Active ingredient FSN> in \<Manufactured dose form FSN> (medicinal product form)

For example,

* Product containing axitinib in oral dose form (medicinal product form)
* Product containing abacavir and lamivudine in oral dose form (medicinal product form)
* Product containing abacavir and lamivudine and zidovudine in oral dose form (medicinal product form)

_Creation of MPF-containing concepts for all possible combinations of active ingredients contained in multiple ingredient products is not recommended at this time (no specific use case has been identified). For example, a product containing three active ingredients would only require creation of one MPF-containing concept. If any of the active ingredients is available as a single ingredient product, or as part of another multiple ingredient concept, then appropriate concepts would be created for those products._

### Preferred Term

\<Active ingredient PT>-containing product in \<Manufactured dose form PT>

\<Active ingredient PT>- and \<Active ingredient PT>-containing product in \<Manufactured dose form PT>

\<Active ingredient PT>- and \<Active ingredient PT>- and \<Active ingredient PT>-containing product in \<Manufactured dose form PT>

For example,

* Axitinib-containing product in oral dose form
* Abacavir- and lamivudine-containing product in oral dose form
* Abacavir- and lamivudine- and zidovudine-containing product in oral dose form

### Synonym

Synonyms matching the FSN are not required.

## Exemplars

<figure><img src="../../../../../../../.gitbook/assets/image (20) (1) (1).png" alt=""><figcaption><p>Stated Template View</p></figcaption></figure>

<figure><img src="../../../../../../../.gitbook/assets/image (22) (1) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 773391004 |Product containing axitinib in oral dose form (medicinal product form)|</p></figcaption></figure>

<figure><img src="../../../../../../../.gitbook/assets/image (23) (1) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 773391004 |Product containing axitinib in oral dose form (medicinal product form)|</p></figcaption></figure>

<figure><img src="../../../../../../../.gitbook/assets/image (24) (1) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 767783007 |Product containing codeine and paracetamol in oral dose form (medicinal product form)|</p></figcaption></figure>

<figure><img src="../../../../../../../.gitbook/assets/image (25) (1) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 767783007 |Product containing codeine and paracetamol in oral dose form (medicinal product form)|</p></figcaption></figure>

<figure><img src="../../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690705.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Medicinal%20Product%20Form%20containing" class="button primary">Provide Feedback</a>
