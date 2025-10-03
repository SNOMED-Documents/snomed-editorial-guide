# Real Clinical Drug (RCD)

## Definition

The representation of a medicinal product marketed by a single organization (supplier) in a single jurisdiction under a single name (which may be a trade or brand name or a generic/non-proprietary name) and which contains the same set precise active ingredient substances and strengths in a single manufactured dose form. It is a subtype of and real world equivalent to the Clinical Drug (CD) class in the international edition of SNOMED CT.

## Use Cases

The following use cases are supported by the Real Clinical Drug concept class:

* Supporting medication process activities: prescribing, dispensing, administration and medication statements
  * In prescribing and in medication statements, especially in situations where the patient should always use a particular Manufactured Product, for reasons of bioavailability (such as a lithium product) or use of administration system (such as an insulin pen)
  * In dispensing and administration, to identify exactly which product was provided/administered
* Reimbursement: national or local systems may set pricing or eligibility against particular manufactured products, regardless of how they are supplied (i.e., with no reference to pack size)
* Allergy checking of specific excipients (if described)
* Pharmacovigilance

## Discussion

The real clinical drug represents the product as most (but not all) regulatory authorities grant the marketing authorization, with the individual packaged products that are marketed into the supply chain in any jurisdiction included _within_ that authorization. A small number of regulatory authorities license each package of a medicinal product separately which is represented by the real packaged clinical drug (see below). Real medicinal products must be represented using the closed world view; they contain **only** the content as stated in the logical definition. Since this class represents real products as authorized in a jurisdiction, description of additional non-defining information, such as excipient substances (flavors, preservatives, sweeteners, etc.) or details about the product name parts or product authorization information and product availability information can be attached to Real Clinical Drug concepts, should a national extension wish to do this. For further details, see the section on Optional Additional Information below.

The real clinical drug is the marketed (therefore "real") instantiation in any one country of the abstract clinical drug in the international edition, and as such, real clinical drugs classify as child concepts of the clinical drug as well as a child concepts of the real medicinal product, if one has been authored. This concept class is, like the clinical drug in the international edition, at the core of the way medicinal products are described, and as such, should always be used in a national extension.

**Existing national terminology equivalents:**

* Actual Medicinal Product in NHS dm+d and Belgian SAM
* Trade Product Unit of Use in in AMT/NZULM
* Semantic Branded Drug (SBD) in RxNorm
* HPK class in the Dutch Z-Index
* Medicinal Product (MP) class in CCDD, the Canadian Clinical Drug Dataset

## Attributes

The real clinical drug class inherits from the clinical drug class in the international edition, and the product name and supplier from the real medicinal product class.

In the following table, two relationship groups (marked with \*) are described: one for presentation strength, and one for concentration strength. The appropriate relationship group type(s) should be selected based on the real product being described. A liquid product being described using a presentation strength in a national extension should follow the pattern used for "[concentration and presentation strength clinical drugs in the national extension](../../../../../authoring/pharmaceutical-and-biologic-product/308610770.html)" in this specification.

***

| Semantic tag      | (real clinical drug)                                                                                                                                                                                                          |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition status | `900000000000073002 \|Sufficiently defined concept definition status (core metadata concept)\|` — This can only be the case if extensions author concepts to represent product names and manufacturer/supplier organisations. |

| Attribute   | `411116001 \|Has manufactured dose form\|`                                                                                                                                   |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range       | `< 736542009 \|Pharmaceutical dose form (dose form)\|`                                                                                                                       |
| Cardinality | 1..1                                                                                                                                                                         |
| Notes       | This is the finished dose form that the manufactured product is presented in by the manufacturer, before any transformation into an administrable dose form has taken place. |

| Attribute   | `42139005 \|Count of base of active ingredient\|`                                                              |
| ----------- | -------------------------------------------------------------------------------------------------------------- |
| Range       | INT (integer)                                                                                                  |
| Cardinality | 1..1                                                                                                           |
| Notes       | This attribute provides the number of base active ingredient substances present in the real medicinal product. |

| Attribute   | `763032000 \|Has unit of presentation\|`                                                                                                                                                                                                                               |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range       | `< 732935002 \|Unit of presentation\|`                                                                                                                                                                                                                                 |
| Cardinality | 0..1                                                                                                                                                                                                                                                                   |
| Notes       | This is the discrete countable entity that the real clinical drug is presented in; it should be valued for all concepts where presentation strength is used and for those real clinical drugs where both concentration strength and presentation strength is required. |

| Attribute                       | `1148793005 \|Unit of presentation size quantity\|`                                                                                                                                    |
| ------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range                           | DEC (decimal)                                                                                                                                                                          |
| Cardinality (within role group) | 0..1                                                                                                                                                                                   |
| Notes                           | This is the volume of liquid that the unit of presentation contains. Should be valued for real clinical drugs where both concentration strength and presentation strength is required. |

| Attribute                       | `320091000221107 \|Unit of presentation size unit\|`                                                                                                                                                                                 |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Range                           | `< 767524001 \|Unit of measure (qualifier value)\|`                                                                                                                                                                                  |
| Cardinality (within role group) | 0..1                                                                                                                                                                                                                                 |
| Notes                           | This is the unit of measure for the volume of liquid that the unit of presentation contains (usually millilitres). Should be valued for real clinical drugs where both concentration strength and presentation strength is required. |

| Attribute   | `774158006 \|Has product name\|`                                                                                                                                                                                                    |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range       | `< 774167006 \|Product name (product name)\|`                                                                                                                                                                                       |
| Cardinality | 1..1                                                                                                                                                                                                                                |
| Notes       | The attribute value should represent the (authorised) product name; this may or may not be a trademarked name and is often referred to as the brand name. Extensions must author product name concepts using the root of 774167006. |

| Attribute   | `774159003 \|Has supplier\|`                                                                                                                                                                                                                                                     |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range       | `< 774164004 \|Supplier (supplier)\|`                                                                                                                                                                                                                                            |
| Cardinality | 1..1                                                                                                                                                                                                                                                                             |
| Notes       | The attribute value should represent the holder of the marketing authorisation or authorisation for supply; this may or may not be the organisation responsible for the actual manufacture of the product. Extensions must author supplier concepts using the root of 774164004. |

***

#### Role group — for presentation strength \[1..\*]

(One per precise active ingredient)

| Role Group Attribute            | `762949000 \|Has precise active ingredient\|`                                                                                                        |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range                           | `< 105590001 \|Substance\|`                                                                                                                          |
| Cardinality (within role group) | 1..1                                                                                                                                                 |
| Notes                           | This is a precise active ingredient substance that the concept contains. In each role group, only one precise active ingredient substance is stated. |

| Role Group Attribute            | `732943007 \|Has basis of strength substance\|`                                                                                               |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Range                           | `< 105590001 \|Substance\|`                                                                                                                   |
| Cardinality (within role group) | 1..1                                                                                                                                          |
| Notes                           | The basis of strength substance that the concept uses. Always stated explicitly, even if the same as the precise active ingredient substance. |

| Role Group Attribute            | `1142135004 \|Has presentation strength numerator value\|`                     |
| ------------------------------- | ------------------------------------------------------------------------------ |
| Range                           | DEC (decimal)                                                                  |
| Cardinality (within role group) | 1..1                                                                           |
| Notes                           | The amount of basis of strength substance present in one unit of presentation. |

| Role Group Attribute            | `732945000 \|Has presentation strength numerator unit\|`                                               |
| ------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Range                           | `< 767524001 \|Unit of measure (qualifier value)\|`                                                    |
| Cardinality (within role group) | 1..1                                                                                                   |
| Notes                           | The unit of measure for the amount of basis of strength substance present in one unit of presentation. |

| Role Group Attribute            | `1142136003 \|Has presentation strength denominator value\|`                                    |
| ------------------------------- | ----------------------------------------------------------------------------------------------- |
| Range                           | DEC (decimal)                                                                                   |
| Cardinality (within role group) | 1..1                                                                                            |
| Notes                           | Should be “one” since the numerator refers to amount of substance per one unit of presentation. |

| Role Group Attribute            | `732947008 \|Has presentation strength denominator unit\|`                                                                        |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Range                           | `< 767524001 \|Unit of measure (qualifier value)\|`                                                                               |
| Cardinality (within role group) | 1..1                                                                                                                              |
| Notes                           | Should be the unit of presentation (`< 732935002 \|Unit of presentation\|`). All units of presentation are subtypes of 767524001. |

***

#### Role group — for concentration strength \[1..\*]

(One per precise active ingredient)

| Role Group Attribute            | `762949000 \|Has precise active ingredient\|`                                        |
| ------------------------------- | ------------------------------------------------------------------------------------ |
| Range                           | `< 105590001 \|Substance\|`                                                          |
| Cardinality (within role group) | 1..1                                                                                 |
| Notes                           | A precise active ingredient substance the concept contains. Only one per role group. |

| Role Group Attribute            | `732943007 \|Has basis of strength substance\|`                                              |
| ------------------------------- | -------------------------------------------------------------------------------------------- |
| Range                           | `< 105590001 \|Substance\|`                                                                  |
| Cardinality (within role group) | 1..1                                                                                         |
| Notes                           | Basis of strength substance used. Always explicit even if same as precise active ingredient. |

| Role Group Attribute            | `1142138002 \|Has concentration strength numerator value\|`            |
| ------------------------------- | ---------------------------------------------------------------------- |
| Range                           | DEC (decimal)                                                          |
| Cardinality (within role group) | 1..1                                                                   |
| Notes                           | Amount of basis of strength substance present in one denominator unit. |

| Role Group Attribute            | `733725009 \|Has concentration strength numerator unit\|` |
| ------------------------------- | --------------------------------------------------------- |
| Range                           | `< 767524001 \|Unit of measure (qualifier value)\|`       |
| Cardinality (within role group) | 1..1                                                      |
| Notes                           | Unit of measure for numerator value.                      |

| Role Group Attribute            | `1142137007 \|Has concentration strength denominator value\|` |
| ------------------------------- | ------------------------------------------------------------- |
| Range                           | DEC (decimal)                                                 |
| Cardinality (within role group) | 1..1                                                          |
| Notes                           | Should be “one” since numerator is per one denominator unit.  |

| Role Group Attribute            | `733722007 \|Has concentration strength denominator unit\|`               |
| ------------------------------- | ------------------------------------------------------------------------- |
| Range                           | `< 767524001 \|Unit of measure (qualifier value)\|`                       |
| Cardinality (within role group) | 1..1                                                                      |
| Notes                           | The unit of the denominator “one” (usually an SI unit of mass or volume). |

***

For real clinical drugs that have two or more active ingredient substances that are modifications of the same base substance **and where** MP precisely concepts are required in the national extension, and for single ingredient product concepts where the active substance is an ingredient in these multiple modification multi-ingredient products, the following extra ingredient count attribute is required in order to support correct relationships generated by the MRCM:

| <p>Attribute: </p><p>1142141006 | Count of base and modification pair |</p> | INT (integer) 1..1 Range Cardinality |
| --------------------------------------------------------------------------- | ------------------------------------ |

For concepts that have two or more active ingredient substances that are modifications of the same base active ingredient substance (i.e., parent ingredient substance) **and** where one is a further modification of the other (for example, a multi-ingredient product containing both dexamethasone phosphate and dexamethasone sodium phosphate, where the dexamethasone phosphate is a modification of dexamethasone (base) and dexamethasone sodium phosphate is a further modification of the dexamethasone phosphate) **and where** MP precisely concepts are required in the national extension, and for single ingredient product concepts where the active substance is an ingredient in these multiple modification multi-ingredient products, the following extra ingredient count attribute will be required in order to support correct relationships generated by the MRCM:

| <p>Attribute: </p><p>1142140007 | Count of active ingredient |</p> | INT (integer) 1..1 Range Cardinality |
| ------------------------------------------------------------------ | ------------------------------------ |

**Note** : The cardinalities given in the above table are for concepts in the RCD class. These cardinalities may be stricter than those in the MRCM, which typically apply across a broader range of concepts.

## Example Diagrams

Some examples of real clinical drug concepts are shown below.

#### **Stated template view:**

<figure><img src="../../../../../.gitbook/assets/image (26) (1).png" alt=""><figcaption><p><em>Template for a real clinical drug</em></p></figcaption></figure>

#### **Example:** single active ingredient substance branded product (Zocor) (presentation strength): stated view followed by the inferred view

<figure><img src="../../../../../.gitbook/assets/image (27) (1).png" alt=""><figcaption><p><em>Single active ingredient substance (presentation strength) real clinical drug example - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (28) (1).png" alt=""><figcaption><p><em>Single active ingredient substance (presentation strength) real clinical drug example - inferred view</em></p></figcaption></figure>

#### **Example: multiple active ingredient substance (presentation strength) branded product (Inegy): stated view followed by the inferred view**

<figure><img src="../../../../../.gitbook/assets/image (29) (1).png" alt=""><figcaption><p><em>Multiple active ingredient substance (presentation strength) real clinical drug example - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610783.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (30) (1).png" alt=""><figcaption><p><em>Multiple active ingredient substance (presentation strength) real clinical drug example - inferred view</em></p></figcaption></figure>

**Example:** single active ingredient substance branded product (Canesten) (concentration strength): stated view followed by the inferred view

<figure><img src="../../../../../.gitbook/assets/image (31) (1).png" alt=""><figcaption><p><em>Single active ingredient substance (concentration strength) real clinical drug example - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610812.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (32) (1).png" alt=""><figcaption><p><em>Single active ingredient substance (concentration strength) real clinical drug example - inferred view</em></p></figcaption></figure>

#### **Example:** single active ingredient substance product (Gentamicin ampule (Hospira)) (concentration and presentation strength) _with_ equivalent clinical drug: stated view followed by the inferred view

In this example, a concentration and presentation strength clinical drug has been authored in the national extension, and therefore, the real clinical drug classifies under this concept.

<figure><img src="../../../../../.gitbook/assets/image (33) (1).png" alt=""><figcaption><p><em>Single active ingredient substance (concentration and presentation strength)</em>with <em>equivalent clinical drug - real clinical drug example - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610810.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (34) (1).png" alt=""><figcaption><p><em>Single active ingredient substance (concentration and presentation strength)</em>with <em>equivalent clinical drug - real clinical drug example - inferred view</em></p></figcaption></figure>

#### **Example:** single active ingredient substance product (Gentamicin vial (Hospira)) (concentration and presentation strength) _without_ equivalent clinical drug: stated view followed by the inferred view

In this example, a concentration and presentation strength clinical drug has been NOT authored in the national extension, and therefore, the real clinical drug classifies under the concentration strength concept in the international edition.

<figure><img src="../../../../../.gitbook/assets/image (35) (1).png" alt=""><figcaption><p><em>Single active ingredient substance (concentration and presentation strength)</em>without <em>equivalent clinical drug - real clinical drug example - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (36) (1).png" alt=""><figcaption><p><em>Single active ingredient substance (concentration and presentation strength)without equivalent clinical drug - real clinical example - inferred view</em></p></figcaption></figure>

## Optional Additional Information

National extensions that function as national medicinal product dictionaries may require information that extends beyond the characteristics of the product as described here in this specification for real clinical drugs. Product characteristics can be included _within_ the SNOMED CT structure using attributes and values, whereas knowledge about the product should be managed _alongside_ the SNOMED CT structure (e.g., in a reference set), and relationships between identification systems should be managed in cross maps.

* Product characteristics may include describing excipient substances to support allergy or intolerance checking. Excipient substance roles may include flavors, colors, preservatives, and stabilizers/fillers.
* Knowledge about the product may include usage information, such as availability within the supply chain, licensing/authorization category and/or legal status of supply and prescribability information including reimbursement categories
* Other identification systems for a real clinical drug may include licensing/authorization number or Global Trade Identification Number (GTIN)

In jurisdictions where repackaging and/or _parallel importing_ are authorised, a national extension may wish to consider having a relationship between the repackaged or parallel imported real clinical drug and the real clinical drug supplied by the original manufacturer, if that is present within the jurisdiction.

## IDMP Compatibility

For most authorised medicinal products, this class is roughly equivalent to the core Medicinal Product class, with its MPID identification in ISO 11615 of IDMP. However, the Medicinal Product class in IDMP explicitly includes combination (kit) products, whereas this model describes combination products as packaged products only. Implementation considerations may require combination products to be available to users alongside clinical drug and real clinical drug concepts; mechanisms, such as the use of reference sets, can support this requirement.

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Real%20Clinical%20Drug%20%28RCD%29" class="button primary">Provide Feedback</a>
