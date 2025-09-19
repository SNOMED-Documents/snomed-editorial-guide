# Real Medicinal Product (RMP)

## Real Medicinal Product (RMP)

## Definition

The representation of a medicinal product marketed by a single organisation (supplier) in a single jurisdiction under a single name (which may be a trade or brand name) and which contains the same set of active ingredient substances, regardless of any modification of those active ingredient substances. It is a subtype of, and real world equivalent to, the Medicinal Product Only (MP only) class in the international core.

## Use Cases

The following use cases are supported by the Real Medicinal Product concept class:

* Describing medication statements for a medication profile when the detail of the exact product used is not known; e.g., "patient states they used Ventolin for 5 years in childhood"
* Decision support and protocol/guideline management may have a use case for this class (for example, to change presentation or strength within a product family)
* Pharmacovigilance (abstract representation of a manufactured medicinal product)

## Discussion

The real medicinal product class is a grouper concept for products containing the same set of active ingredient substance(s) and marketed under the same name by the same supplier.

### **Single ingredient substance branded products**

The RMP "Zocor (product)" shown in a taxonomic view in Figure 1 below presents products marketed by Organon Pharma UK Limited under a single name (Zocor) and containing only simvastatin as the active ingredient substance and shows the RCD concepts associated with it:

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610741.png" alt=""><figcaption><p><em>Figure 1: Diagram showing a branded single ingredient substance real medicinal product and its supporting real clinical drug concepts</em> (Note: not all possible real clinical drug concepts are shown.)</p></figcaption></figure>

### **Single ingredient generic products**

For those products without a unique (i.e., invented) product name, where the product uses the international non-proprietary name of the active substance as its product name (i.e., so called _generic_ products), extensions may choose not to populate the Real Medicinal Product class, as shown below, with each RCD being associated directly with the CD in the International content:

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610740.png" alt=""><figcaption><p><em>Figure 2: Example of real clinical drug "generic" products where a real medicinal product concept has not be authored</em></p></figcaption></figure>

Alternatively, for products without a unique (i.e. invented) product name (_generic_ products) a national extension may choose to populate the Real Medicinal Product using the generic name AND supplier, since this gives a unique RMP concept, as shown below:

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610760.png" alt=""><figcaption><p><em>Figure 3:</em>Example of real clinical drug "generic" products where a <em>real medicinal product concept has been authored using product and manufacturer name</em></p></figcaption></figure>

Note that here the product name attribute is valued as "simvastatin", which in text looks similar to both the substance concept 387584000 | Simvastatin (substance) | and to the two medicinal product concepts 96304005 | Product containing simvastatin (medicinal product) | and 777537002 | Product containing only simvastatin (medicinal product) |. But it is a different concept and has its own semantic tag of "product name"; it is therefore a different concept (unit of thought): Simvastatin (product name).777537002 | Product containing only simvastatin (medicinal product) |

### **Multi-Ingredient substance branded products**

One of the fundamentals of a Real Medicinal Product is that it represents a single set of active ingredient substances, reflecting its associated MP only class that also represents a single set of active ingredient substances, without dose form or strength information.

The RMP "Inegy (product)" shown in a taxonomic view in Figure 2 below presents products marketed by Organon Pharma UK Limited under a single name (Inegy) and containing only simvastatin AND ezetimibe as the active ingredient substances, and showing the RCD concepts associated with it:

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610759.png" alt=""><figcaption><p><em>Figure 4: Diagram showing a branded multi-ingredient substance real medicinal product and its supporting real clinical drug concepts (note, not all possible real clinical drug concepts are shown)</em></p></figcaption></figure>

Not all authorised medicinal products that share the same (invented) product name will relate to a Real Medicinal Product, especially for over the counter (OTC) medicines, where a commercial "brand family" may contain products with different active ingredient sets which would therefore have different MP only representations. For example, some cough and cold product ranges span expectorant products, cough suppressants, antipyretics and decongestant products, with different sets of active ingredients in each but all sharing the same brand name.

In the example below, the three real clinical drug products all share the same product name ("Benylin®") in one jurisdiction, but they do not relate to a single real medicinal product due to differences in their active ingredient substances.

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610739.png" alt=""><figcaption><p><em>Figure 5: Example of branded real clinical drug products sharing the same product name but not relating to a Real Medicinal Product due to differences in their set of active ingredient substances</em></p></figcaption></figure>

A national extension may choose to populate RMPs for "brand families" that contain products with different active ingredient sets by extending the product name concept to include enough detail to scope just a single active ingredient set, as shown below:

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610738.png" alt=""><figcaption><p><em>Figure 6: Example of branded real clinical drug products relating to appropriate real medicinal products by authoring of specific product name concepts</em></p></figcaption></figure>

**Existing national terminology equivalents for real medicinal product:**

* Trade family in NHS dm+d
* Trade Product (TP) in AMT/NZULM
* Brand Name (BN) in RxNorm (possibly)

## Attributes

The following attributes apply to Real Medicinal Product (RMP) concepts in a national extension. The RMP class has two attributes inherited from the Medicinal Product (only) class in the international content and two additional attributes.

| Semantic tag                                                  | (real medicinal product)                                                                                                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition status                                             | 900000000000073002 \| Sufficiently defined concept definition status \|                                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Attribute 1142139005 \| Count of base of active ingredient \| | INT (Integer) 1..1 This attribute provides the number of base active ingredient substances present in the medicinal product Range Cardinality Notes                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Attribute 774159003 \| Has supplier \|                        | Extensions must author concepts to value supplier organisation information within their extension using the root of 774164004 \| Supplier (supplier) \| from the Qualifier hierarchy 1..1 The attribute value should represent the holder of the marketing authorisation or authorisation for supply; this may or may not be the organisation responsible for the actual manufacture of the product (see section below). Range <774164004\|Supplier (supplier)\| Cardinality Notes |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Attribute 774158006 \| Has product name \|                    | Extensions must author product name concepts within their extension using the root of 774167006 \| Product name (product name) \| from the Qualifier hierarchy 1..1 The attribute value should represent the (authorised) product name; this may (or may not) be a trademarked name, and is often referred to as the "brand name" (see section below). Range <774167006\|Product name (product name)\| Cardinality Notes                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Role Group                                                    | Attribute 127489000 \| Has active ingredient \|                                                                                                                                                                                                                                                                                                                                                                                                                                    | Excluding concepts representing structural groupers, dispositions, or combined substances 1..\* There is no technical limit on the number of \| Has active ingredient \| attributes that may be added to a concept; a practical limit may be imposed by national extensions. In order to classify correctly to the international content, this attribute value should represent the base ingredient substance, not a modification, unless explicitly identified as an exception and requiring an association to MP precisely concept. Range <105590001\|Substance\| Cardinality Notes This attribute describes the set of active ingredient substances that the concept minimally contains. A set of active ingredient substances may well have only one member. |

**Note** : The cardinalities given in the above table are for concepts in the RMP class. These cardinalities may be stricter than those in the MRCM, which typically apply across a broader range of concepts.

## Example Diagrams

**Stated template view:**

\*\*

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610737.png" alt=""><figcaption><p>**</p></figcaption></figure>

_Figure 7: Real Medicinal Product (RMP) stated template view_

#### **Example:** single active ingredient substance branded product (Zocor): state view followed by the inferred view

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610755.png" alt=""><figcaption><p><em>Figure 8: Single active ingredient substance real medicinal product example stated view</em></p></figcaption></figure>

\*\* \_

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610754.png" alt=""><figcaption><p>_**</p></figcaption></figure>

_Figure 9: Single active ingredient substance real medicinal product example inferred view_

#### **Example: multiple active i ngredient substance branded product (Inegy): stated view followed by the inferred view**

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610753.png" alt=""><figcaption><p><em>Figure 10: Multiple active ingredient substance real medicinal product example stated view</em></p></figcaption></figure>

\*\* \_

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610752.png" alt=""><figcaption><p>_**</p></figcaption></figure>

_Figure 11: Multiple active ingredient substance real medicinal product example inferred view_

## IDMP Compatibility

There is no identified representation of a class similar to the Real Medicinal Product concept class in IDMP despite there being (a possible) pharmacovigilance use case for this class.
