# Real Packaged Clinical Drug (RPCD)

## Real Packaged Clinical Drug (RPCD)

## Definition

The representation of a medicinal product as it is supplied in a package by a single organisation (manufacturer or supplier) in a single jurisdiction under a single name (which may be a trade or brand name) for placement into the supply chain. It is a subtype of, and real world equivalent to, the Packaged Clinical Drug (PCD) class.

## Use Cases

The following use cases are supported by the Real Packaged Clinical Drug concept class:

* Describing medication process activities: prescribing, dispensing, administration and medication statements; of these, dispensing and administration will use this concept when it is available to clearly state which actual packaged product (or content from it) was used/supplied to the patient (with batch/lot and expiry information if required, either manually or by automatic identification and data capture (AIDC), for example, scanning the bar code on the package)
* Compliance monitoring, using pack size information to calculate whether a patient is following the dosage instructions correctly (how quickly a repeat supply of a package of medication is required)
* Anti-counterfeiting: in support of initiatives such as the Falsified Medicines Directive (see amended Directive 2001/83/EC) using AIDC and which requires scanning of medicines at the point of supply (to the patient)
* Reimbursement: national or local systems may set pricing or eligibility against actual packaged products
* Pharmacovigilance – especially for product defects and labeling issues
* The association between the clinical representation of medicinal products and their representation in the supply chain for supply chain management

## Discussion

The real packaged clinical drug represents the product as its packaged products that are marketed into the supply chain in any jurisdiction. A small number of regulatory authorities license medicines at this level, with each package having a separate authorisation; others allow all the different package sizes to be authorised by the single authorisation of the RCD. Real packaged clinical drugs must be represented using the closed world view; they contain \_**only** \_the content as stated in the logical definition. Since this class represents real product packages as authorised in a jurisdiction, description of additional non-defining information, such as excipient substances (flavours, preservatives, sweeteners, etc.) or details about the product name parts or product authorisation information and product availability information can be attached to real packaged clinical drug concepts, should a national extension wish to do this.

The real clinical packaged drug is the marketed (therefore "real") instantiation in any one country of the abstract packaged clinical drug in the international edition, and as such, real packaged clinical drugs classify as child concepts of the packaged clinical drug, if the national extension has authored these concepts.

As described above in the PCD section, this national extension model does not represent intermediate layers of packaging; it represents only the outer package used in the supply chain.

National extensions that require real packaged clinical drug concepts are advised to define their real packaged clinical drug concepts using real clinical drug concepts from their national extension. This allows grouping of package concepts with their associated real clinical drug using the [774160008 | Contains clinical drug (attribute)|](http://snomed.info/id/774160008) value and information from that (for example, excipient information) can be transferred through that composition relationship if required.

**Existing national terminology equivalents:**

* Actual Medicinal Product Pack (AMPP) in NHS dm+d and Belgian SAM
* Trade Product Pack (TPP) in in AMT/NZ ULM
* Semantic Branded Drug Pack (BPCK) in RxNorm
* "Product" class in the Dutch Z-Index

## Attributes

The following table describes the attributes for real packaged clinical drugs (RPCDs) that contain one type of clinical drug only. That is, they are NOT combination (multi-component or kit) products.

The real packaged clinical drugs class is related to the real clinical drug class by a composition relationship, and therefore the attribute |Contains real clinical drug (attribute)| is used to make the association between the real packaged clinical drug and the (real) clinical drug it contains.

Representation of real packaged medicinal products should use presentation strength (either only, or in addition to, concentration strength) whenever possible in order to be able to accurately describe the number of presentation units present in the package. The exception is for continuous products such as semi-solid dose forms of creams, gels, etc. where strength pattern 3a is used (see [Ingredient Strength Attributes](../../../../../authoring/pharmaceutical-and-biologic-product/Ingredient-Strength-Attributes_303923286.html)). In all cases, the pack size and pack size unit should relate to the denominator unit of the strength.

| <p><strong>Semantic tag</strong><br><br><br></p>           | (real packaged clinical drug)                                                                                                                                                                                                                                                                                                            |
| ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>Definition status</strong><br><br><br></p>      | <p>900000000000073002 |Sufficiently defined concept definition status (core metadata concept)</p><p><strong>Note</strong>: This can only be the case if extensions author concepts to represent real clinical drugs and/or product names and manufacturer / supplier organisations</p>                                                   |
| **Attribute:**  1142143009 \|Count of clinical drug type\| | <p><strong>Range</strong></p><ul><li>INT (integer)</li></ul><p><strong>Cardinality</strong></p><ul><li>1..1</li></ul><p><strong>Note</strong></p><ul><li>This attribute provides the number (count) of distinct clinical drug (concepts) present in the package.  For all non-combination packages, this value should be "one"</li></ul> |

| <p><strong>Role Group</strong> <br>[1..*]</p><p>(although for all packages other than combination products it is 1..1)</p> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Attribute:** 774160008 \|Contains clinical drug\|                                                                        | <p><strong>Range</strong></p><ul><li>&#x3C; 763158003 |Medicinal product (product)|</li></ul><p><strong>Cardinality</strong></p><ul><li>1..1</li></ul><p><strong>Note</strong></p><ul><li>This attribute value represents the real clinical drug that is contained in the packaged product<br>It is currently not possible to explicitly specify an expression to describe the range of real clinical drugs from a national extension to populate this attribute, since a range cannot currently recognise a set of concepts with a particular semantic tag - in this case "(real clinical drug)".  For the interim, the range is specified as the descendants of the root medicinal product concept: 763158003 |Medicinal product (product)|. </li></ul>                                                                                                                                                                                                          |
| **Attribute:**  1142142004 \|Has pack size\|                                                                               | <p><strong>Range</strong></p><ul><li>INT (integer)</li></ul><p><strong>Cardinality</strong></p><ul><li>1..1</li></ul><p><strong>Note</strong></p><ul><li>This attribute represents the amount or quantity of clinical drug present in the package; for presentation strength it is the number of countable units of presentation in the package; for concentration strength it is the mass or volume of the continuous dose form in the package</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Attribute:**  774163005 \|Has pack size unit\|                                                                           | <p><strong>Range</strong></p><ul><li>&#x3C;  767524001 |Unit of measure (qualifier value)|</li></ul><p><strong>Cardinality</strong></p><ul><li>1..1</li></ul><p><strong>Note</strong></p><ul><li>This attribute value represents the unit of measure of the pack size;  for presentation strength, it is the unit of presentation in the package; for concentration strength, it is the unit of mass (e.g. gram) or volume (e.g. millilitre) of the continuous dose form in the package. <br>More specific range expressions such as "One of EITHER &#x3C;732935002 | Unit of presentation (unit of presentation) -  OR &#x3C;258680008 | Unit of mass (qualifier value) OR &#x3C;258769000 | Unit of volume (qualifier value)" are currently not supported, nor are rules based on the strength patterns that (for example) assert "if the clinical drug has a unit of presentation of 'tablet' then the Has_pack_size_unit will be valued as 'tablet".</li></ul> |

## Example Diagrams

Some examples of real packaged clinical drugs are shown below.

**Stated template view:**

<figure><img src="../../../../../.gitbook/assets/image (44).png" alt=""><figcaption><p><em>Template for a simple real packaged clinical drug</em></p></figcaption></figure>

#### **Example:** simple real packaged clinical drug: stated view followed by the inferred view

<figure><img src="../../../../../.gitbook/assets/image (45).png" alt=""><figcaption><p><em>Example of a real packaged clinical drug - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (46).png" alt=""><figcaption><p><em>Example of a real packaged clinical drug - inferred view</em></p></figcaption></figure>

## Optional Additional Information

As with the real clinical drugs, national extensions may require additional information to be associated with real packaged clinical drugs. This may include characteristics of the packaged product that can be described _within_ the SNOMED CT structure using attributes and values, managed _alongside_ the SNOMED CT structure (e.g., in a reference set) and/or relationships between identification systems should be managed in cross maps.

* Packaged product characteristics may include package/container types (e.g. bottle, box, jar, tube - to support various use cases including robotic dispensing) and administration device supplied in the package (e.g. medicine spoon, vaginal applicator, applicator brush for cutaneous liquid products)
* Knowledge about the product may include usage information such as availability within the supply chain, licensing/authorization category and/or legal status of supply, and prescribability information including reimbursement categories
* Other identification systems for a real packaged clinical drug may include licensing/authorization number, if this is provided for individual packages or Global Trade Identification Number

In jurisdictions where repackaging and/or _parallel importing_ are authorised, a national extension may wish to consider having a relationship between the repackaged or parallel imported real packaged clinical drug and the real clinical drug supplied by the original manufacturer, if that is present within the jurisdiction.

## IDMP Compatibility

This concept as defined is equivalent to the Packaged Medicinal Product of ISO 11615, which in that standard is identified by a PCID. As the representation of the _real world product_ authorised for sale and/or supply that exists for all jurisdictions and which is marketed into the supply chain for use, it is the concept that should form the 1:1 join between representation in the regulatory domain (IDMP) and representation in the clinical domain (SNOMED CT and national medicinal product terminologies), even if some national medicinal product terminologies choose not to represent it, but only an abstraction of it (i.e., the Real Clinical Drug class of concepts).
