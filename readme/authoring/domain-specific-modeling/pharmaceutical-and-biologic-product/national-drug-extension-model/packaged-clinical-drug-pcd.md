# Packaged Clinical Drug (PCD)

## Packaged Clinical Drug (PCD)

## Definition

An abstract representation of a medicinal product as it is supplied in a package for placement into the supply chain, based on description of and quantity of the clinical drug(s) contained within that package.

As an abstract class, the Packaged Clinical Drug is placed on the lefthand side of the overall model, relating directly to the Clinical Drug class in the international core by means of a composition relationship, but its population is the responsibility of national extensions since the amount of content needed to support this internationally would be overwhelming and unmanageable in maintenance and verification.

This definition supports the description of kit or combination products - medicinal products that are composed of more than one clinical drug, such as a package containing fluconazole oral capsules and clotrimazole cream for treatment of vaginal thrush as packaged clinical drugs, and therefore the pack size information for each clinical drug that is a component in the package is grouped together. Further detail on the description of combination products (multi-component or kit products) is given below.

## Use Cases

The following use cases are supported by the Packaged Clinical Drug concept class:

* Reimbursement: national or local systems may set pricing or eligibility against an abstract representation of real packaged products (e.g., for interchangeability and substitution)
* As a linking class from the international core to the Real Packaged Clinical Drug class for any national extension that did not require a Real Clinical Drug class (i.e., if all products are authorised in their packaged form)
* To support description of combination packaged products

## Discussion

Packs of medicinal products must be represented using the closed world view; they contain \_**only** \_the clinical drug content stated. The packaged clinical drug class is related to the clinical drug class by a composition relationship, the package _contains_ the clinical drug. To correctly describe this and so to ensure that pack concepts classify correctly, and so that packs that contain more than one (type of) clinical drug (i.e., combination packs) do not classify as children of packs that contain only one type of clinical drug, it is necessary to use a "clinical drug count" attribute as a proxy for the closed world view, in a similar way to the use of the active ingredient count attribute used for MP only concepts, MPF only concepts, and clinical drug concepts. By using a "count" attribute in the definition of closed world concepts, the count information is machine processable, and therefore, if/when a more expressive description logic becomes available to properly represent the closed world view, then all the count attributes can be used to transfer to the closed world description logic consistently.

<figure><img src="../../../../../.gitbook/assets/image (37) (1).png" alt=""><figcaption><p><em>Diagram of the packaged clinical drug class and its composition relationship to clinical drug, with an example (Zocor)</em></p></figcaption></figure>

The national extension model does not represent intermediate layers of packaging; it represents only the outer package used in the supply chain. Describing _sub-packs_(e.g., tablets within blister sleeves, which are then within a container such as a box) is complex for a description logic based model and is currently out of scope for this initial version of the national extension specification. In most nations, sub-packs are primarily used for supply chain management and reimbursement purposes, and possibly rounding of dispense amounts so that sub-packs are not split. Many medicinal product terminologies do not represent sub-packs. ISO 11615, the Medicinal Product part of the IDMP suite of standards, has a full sub-pack mode, but the sub-packs themselves are not identified concepts and so are not available for mapping, etc.; however, the GS1 implementation of ISO TS 16791 does include identification of sub-packs.

**Existing national terminology equivalents:**

* UK's NHS dm+d this is the Virtual Medicinal Product Pack (VMPP) class
  * The AMT/NZULM it is the Medicinal Product Pack
  * In Ireland, this is in effect those packaged products on the Representative Pricing list
  * The generic pack (GPCK) class in RxNorm

## Attributes

The following table describes the attributes for packaged clinical drugs that contain one type of clinical drug only. That is they are NOT combination (multi-component or kit) products.

The packaged clinical drug class is related to the clinical drug class by a composition relationship, and therefore, the 774160008 | Contains clinical drug (attribute)| is used to make the association between the packaged clinical drug and the clinical drugs it contains.

Representation of packaged medicinal products should use clinical drugs that have presentation strength (either only, or in addition to, concentration strength) whenever possible in order to be able to accurately describe the number of presentation units present in the package. The exception is for continuous products such as semi-solid dose forms of creams, gels, etc. where strength pattern 3a is used (see [Ingredient Strength Attributes](../../../../../authoring/pharmaceutical-and-biologic-product/Ingredient-Strength-Attributes_303923286.html)). In all cases, the pack size and pack size unit should relate to the denominator unit of the strength.

***

<table data-header-hidden><thead><tr><th width="221.40234375"></th><th></th></tr></thead><tbody><tr><td>Semantic tag</td><td>(packaged clinical drug)</td></tr><tr><td>Definition status</td><td><code>900000000000073002 |Sufficiently defined concept definition status (core metadata concept)|</code></td></tr></tbody></table>

<table data-header-hidden><thead><tr><th width="232.62109375"></th><th></th></tr></thead><tbody><tr><td>Attribute</td><td><code>1142143009 |Count of clinical drug type|</code></td></tr><tr><td>Range</td><td>INT (integer)</td></tr><tr><td>Cardinality</td><td>1..1</td></tr><tr><td>Notes</td><td>This attribute provides the number (count) of distinct clinical drug (concepts) present in the package. For all non-combination packages, this value should be “one”.</td></tr></tbody></table>

***

#### Role group \[1..\*]

(although for all packages other than combination products it is 1..1)

<table data-header-hidden><thead><tr><th width="262.99609375"></th><th></th></tr></thead><tbody><tr><td>Role Group Attribute</td><td><code>774160008 |Contains clinical drug|</code></td></tr><tr><td>Range</td><td><code>&#x3C; 763158003 |Medicinal product (product)|</code></td></tr><tr><td>Cardinality</td><td>1..1</td></tr><tr><td>Notes</td><td>This attribute value represents the clinical drug contained in the packaged product. It is currently not possible to explicitly specify an expression to describe the range of clinical drugs to populate this attribute, since a range cannot currently recognise a set of concepts with a particular semantic tag — in this case, (clinical drug). Alternative range expressions could be used based on definitional attributes of a clinical drug. For the interim, the range is specified as descendants of the root medicinal product concept: <code>763158003 |Medicinal product (product)|.</code></td></tr></tbody></table>

***

<table data-header-hidden><thead><tr><th width="257.62109375"></th><th></th></tr></thead><tbody><tr><td>Attribute</td><td><code>1142142004 |Has pack size|</code></td></tr><tr><td>Range</td><td>INT (integer)</td></tr><tr><td>Cardinality</td><td>1..1</td></tr><tr><td>Notes</td><td>Represents the amount or quantity of clinical drug in the package. For presentation strength: the number of countable units of presentation. For concentration strength: the mass or volume of the continuous dose form in the package.</td></tr></tbody></table>

<table data-header-hidden><thead><tr><th width="247.96875"></th><th></th></tr></thead><tbody><tr><td>Attribute</td><td><code>774163005 |Has pack size unit|</code></td></tr><tr><td>Range</td><td><code>&#x3C; 767524001 |Unit of measure (qualifier value)|</code></td></tr><tr><td>Cardinality</td><td>1..1</td></tr><tr><td>Notes</td><td>This attribute represents the unit of measure of the pack size. For presentation strength: the unit of presentation in the package. For concentration strength: the unit of mass (e.g. gram) or volume (e.g. millilitre) of the continuous dose form in the package. More specific range expressions (e.g. “One of EITHER <code>&#x3C;732935002 |Unit of presentation| OR &#x3C;258680008 |Unit of mass| OR &#x3C;258769000 |Unit of volume|</code>”) are not currently supported, nor are conditional rules (e.g. “if the clinical drug has a unit of presentation of tablet then the pack size unit must be tablet”).</td></tr></tbody></table>

***

## Example Diagrams

Some examples of packaged clinical drug (PCD) concepts are shown below.

**Stated template view:**

<figure><img src="../../../../../.gitbook/assets/image (38).png" alt=""><figcaption><p><em>Template for simple packaged clinical drug</em></p></figcaption></figure>

#### **Example:** single active ingredient substance presentation strength packaged clinical drug: stated view followed by the inferred view

<figure><img src="../../../../../.gitbook/assets/image (39).png" alt=""><figcaption><p><em>Example of a presentation strength packaged clinical drug - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (40).png" alt=""><figcaption><p><em>Example of a presentation strength packaged clinical drug - inferred view</em></p></figcaption></figure>

#### **Example:** single active ingredient substance presentation strength packaged clinical drug: stated view followed by the inferred view

<figure><img src="../../../../../.gitbook/assets/image (41).png" alt=""><figcaption><p><em>Example of a concentration strength packaged clinical drug - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (42).png" alt=""><figcaption><p><em>Example of a concentration packaged clinical drug - inferred view</em></p></figcaption></figure>

## Optional Additional Information

The following information may be additionally used to describe characteristics of the packaged clinical drug concept in a national extension:

* Package/container type (e.g., bottle, box, jar, tube)
* Administration device supplied in the package (e.g., medicine spoon, vaginal applicator, applicator brush for cutaneous liquid products)

## IDMP Compatibility

There is no representation of a class similar to the Packaged Clinical Drug concept class; the primary use case for this class beyond support for generic representation of combination products is reimbursement, which is out of scope of IDMP. Combination products in their entirety are only represented in IDMP in their authorised form; there is no PhP type representation for them.

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Packaged%20Clinical%20Drug%20%28PCD%29" class="button primary">Provide Feedback</a>
