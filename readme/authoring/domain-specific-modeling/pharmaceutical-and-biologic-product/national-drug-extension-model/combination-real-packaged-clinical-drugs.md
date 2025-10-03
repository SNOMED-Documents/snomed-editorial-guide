# Combination (Real) Packaged Clinical Drugs

## Definition

The representation of a medicinal product as it is supplied in a package that contains within the package more than one type of clinical drug.

## Use Cases

The use cases supported by the Combination (Real) Packaged Clinical Drug concept type are the same as those for the basic real packaged clinical drug with the additional detail that administration records may wish to identify which of the particular component clinical drugs were administered at any particular point in time of the administration event (using AIDC or similar).

## Discussion

For abstract concepts, the combination packaged clinical drug contains two or more different clinical drugs.

For real concepts, the combination real packaged clinical drug contains two or more different real clinical drugs. The package is placed in the supply chain using a single name (which may be a trade or brand name) by a single supplier organization, even if one or more of the component real clinical drugs is sourced from a different organization. For this reason, the 774158006 |Has product name| and 774159003 |Has supplier| attributes are optionally included.

A combination packaged clinical drug may also be called a _component product_ or a _multi-component package_ as the product itself is a package that contains more than one type of component element (clinical drug) within it. It may also be known as or a _kit_ or a _combination medicinal product_. Occasionally a combination packaged clinical drug may be known as a _compound product_ , but this term risks being confused with products that are extemporaneously compounded by a pharmacist from a formula provided by the prescriber for an individual patient (sometimes also known as _magistral products_).

Examples of combination packaged clinical drug include a package each containing:

* clotrimazole cutaneous cream and one or more clotrimazole vaginal tablets for treatment of vaginal candidiasis
* clotrimazole cutaneous cream and one or more fluconazole oral capsules for treatment of vaginal candidiasis
* combinations of ethinylestradiol and levonorgestrel tablets in different strengths and which may also include inert tablets for oral contraception (note that in this example, the components are themselves multi-ingredient items)
* amoxicillin, clarithromycin and lansoprazole for treatment of Helicobacter infection
* a budesonide dispersible tablet and the vehicle to disperse it in to make a rectal solution for treatment of colitis
* rasburicase 1.5 mg powder for solution for injection and the diluent solution

This specification for national drug extensions recommends that a combination packaged clinical drug should be represented only as packaged products (real packaged clinical drugs, and if an abstract representation is required, as packaged clinical drugs), with their individual components represented as clinical drugs. For practical implementation of a national terminology, mechanisms such as reference sets may be used to include combination packaged clinical drug with other classes of medicinal product (such as clinical drugs) to aid users in finding and selecting these products.

The following diagram gives an example of how the packaged medicinal product classes should be used to describe combination medicinal products:

<figure><img src="../../../../../.gitbook/assets/image (47).png" alt=""><figcaption><p><em>Diagram of options for a national extension describing combination real packaged clinical drugs</em></p></figcaption></figure>

In some representations of combination packages, and particularly in ISO 11615 in IDMP, a _combined dose form_ concept is used in the name of the combination product (for example, pessary and cream). Although useful as a concept to describe the dose form using a single attribute and value, a combination dose form concept does not easily support knowing which component has which dose form. The model used here, whereby each clinical drug is described with its appropriate dose form and they are brought together into the packaged product containing the components, does not require the use of combination dose form concepts.

For those combination packages that contain a diluent as an item in the package, national extensions may decide not to explicitly describe the diluent as a component but merely to describe its presence in the text of the fully specified name for the real packaged medicinal product; alternatively, the national extension may author a _diluent_ clinical drug concept and use that as one of the components of the combination product. If the constitution of the diluent is known (e.g., water for injections, 0.9% sodium chloride solution for injection), the clinical drug for the diluent can be explicitly described. Dual chamber products containing the two components (where one is the diluent) in a single unit of presentation can be described as combination products if required.

## Attributes

The following table describes the attributes for combination (real) packaged clinical drugs in a national extension.

The (real) packaged clinical drug class is related to the clinical drug class by a composition relationship, and therefore, the 774160008 | Contains clinical drug (attribute)| is used to make the association between the packaged clinical drug and the clinical drugs it contains.

Representation of packaged medicinal products should use Clinical Drugs that have presentation strength (either only, or in addition to, concentration strength) whenever possible in order to be able to accurately describe the number of presentation units present in the package. The exception is for continuous products such as semi-solid dose forms of creams, gels, etc. where strength pattern 3a is used (see [Ingredient Strength Attributes](../../../../../authoring/pharmaceutical-and-biologic-product/Ingredient-Strength-Attributes_303923286.html)). In all cases, the pack size and pack size unit should relate to the denominator unit of the strength.

Here’s the combined Packaged Clinical Drug (PCD) / Real Packaged Clinical Drug (RPCD) table in the same GIRBook-ready style (no merged cells, consistent with your other six):

***

| Semantic tag      | (packaged clinical drug) OR (real packaged clinical drug)                                                                                                                                                                                                      |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition status | `900000000000073002 \|Sufficiently defined concept definition status (core metadata concept)\|` — Note: This can only be the case if extensions author concepts to represent real clinical drugs and/or product names and manufacturer/supplier organisations. |

| Attribute   | `1142143009 \|Count of clinical drug type\|`                                                                                                            |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range       | INT (integer)                                                                                                                                           |
| Cardinality | 1..1                                                                                                                                                    |
| Notes       | Provides the number (count) of distinct clinical drug concepts present in the package. For combination packages, this value should be greater than one. |

| Attribute   | `774158006 \|Has product name\|`                                                                                                                                                                                                                                                                                                                 |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Range       | `< 774167006 \|Product name (product name)\|`                                                                                                                                                                                                                                                                                                    |
| Cardinality | 0..1                                                                                                                                                                                                                                                                                                                                             |
| Notes       | The attribute value should represent the (authorised) product name; may or may not be trademarked, often called the “brand name”. Should only be valued in rare cases when the combination product’s name differs from the names of its component real clinical drugs. Extensions must author product name concepts using the root of 774167006. |

| Attribute   | `774159003 \|Has supplier\|`                                                                                                                                                                                                                                                                                                                                                                                             |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Range       | `< 774164004 \|Supplier (supplier)\|`                                                                                                                                                                                                                                                                                                                                                                                    |
| Cardinality | 0..1                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Notes       | The attribute value should represent the holder of the marketing authorisation or authorisation for supply; may or may not be the organisation responsible for actual manufacture. Should only be valued in rare cases when the supplier for the combination product differs from the suppliers of its component real clinical drugs. Extensions must author supplier organisation concepts using the root of 774164004. |

***

#### Role group \[1..\*] (for combination packaged clinical drugs)

| Role Group Attribute | `774160008 \|Contains clinical drug\|`                                                                                                                                                                                                                                                                                                                       |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Range                | `< 763158003 \|Medicinal product (product)\|`                                                                                                                                                                                                                                                                                                                |
| Cardinality          | 1..1                                                                                                                                                                                                                                                                                                                                                         |
| Notes                | Represents the real clinical drug contained in the packaged product. It is currently not possible to explicitly specify a range of (real) clinical drugs from a national extension to populate this attribute, since a range cannot recognise a semantic tag. For now, the range is specified as descendants of `763158003 \|Medicinal product (product)\|`. |

| Role Group Attribute | `1142142004 \|Has pack size\|`                                                                                                                                                                                                   |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range                | INT (integer)                                                                                                                                                                                                                    |
| Cardinality          | 1..1                                                                                                                                                                                                                             |
| Notes                | Represents the quantity of clinical drug in the role group present in the package. For presentation strength: number of countable units of presentation. For concentration strength: mass or volume of the continuous dose form. |

| Role Group Attribute | `774163005 \|Has pack size unit\|`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Range                | `< 767524001 \|Unit of measure (qualifier value)\|`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Cardinality          | 1..1                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Notes                | Represents the unit of measure of the pack size in the role group. For presentation strength: the unit of presentation in the package. For concentration strength: the unit of mass (e.g. gram) or volume (e.g. millilitre) of the continuous dose form. More specific range expressions (e.g. “One of either `<732935002 \|Unit of presentation\| OR <258680008 \|Unit of mass\| OR <258769000 \|Unit of volume\|`”) are not supported, nor are conditional rules (e.g. “if the clinical drug has a unit of presentation of tablet then Has pack size unit = tablet”). |

***

## Example Diagrams

#### Example: combination packaged clinical drug: stated view followed by the inferred view

<figure><img src="../../../../../.gitbook/assets/image (48).png" alt=""><figcaption><p><em>Example of a combination packaged clinical drug - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (49).png" alt=""><figcaption><p><em>Example of a combination packaged clinical drug - inferred view</em></p></figcaption></figure>

#### Example: combination real packaged clinical drug: stated view followed by the inferred view

<figure><img src="../../../../../.gitbook/assets/image (50).png" alt=""><figcaption><p><em>Example of a combination real packaged clinical drug - stated view</em></p></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610841.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (51).png" alt=""><figcaption><p><em>Example of a combination real packaged clinical drug - inferred view</em></p></figcaption></figure>

## IDMP Compatibility

Since the ISO 11615 standard treats all Packaged Medicinal Products in the same manner whether they are standard products or combination products, and because the associations between the manufactured item(s) present in the package are described using recursive relationships, the Combination Real Packaged Medicinal Product is equivalent to a Packaged Medicinal Product identified by a PCID. As with the Real Packaged Medicinal Product, the Combination Real Packaged Medicinal Product is a representation of the _real world product_ authorized for sale and/or supply that exists for all jurisdictions and is marketed into the supply chain for use, it is a concept that should form the 1:1 join between representation in the regulatory domain (IDMP) and representation in the clinical domain (SNOMED CT and national medicinal product terminologies) even if some national medicinal product terminologies choose not to represent it.

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Combination%20%28Real%29%20Packaged%20Clinical%20Drugs" class="button primary">Provide Feedback</a>
