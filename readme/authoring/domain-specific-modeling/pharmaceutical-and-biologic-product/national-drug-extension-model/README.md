---
layout:
  width: wide
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
    visible: true
---

# National Drug Extension Model

## National Drug Extension Model

## Model Overview

The diagram below shows the concept classes for the extension model with the related concept classes from the international medicinal product model. No role or grouper classes (i.e., parents of the international Medicinal Product (MP) class) are shown in the diagram. It is expected that all grouping classes (based on substance structure, disposition and therapeutic role) will be inherited from the international release. For all of the classes in the national drug extension model, the closed world view applies. Products are defined using only the active ingredient substances as authorised by the regulatory agency in the particular jurisdiction of use. Packs are defined using only the clinical drug concepts that they are composed of (contain) (see also [Supporting Attributes](../../../../../authoring/pharmaceutical-and-biologic-product/Supporting-Attributes_308610855.html)).

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/308610731.png" alt=""><figcaption><p><em><strong>Figure 1: Diagram of the classes of the SNOMED CT national extension model for Medicinal Products</strong></em></p></figcaption></figure>

_In the diagram, the MP classes are shown in shades of blue, the MPF classes in shades of yellow, the CD classes in shades of green and the PCD classes in shades of orange; the concepts represent the real world medicinal products available within a nation and described within that extension are shown in the brighter shades\*\*._\
\&#xNAN;_\*\*_

## Classes of National Drug Extension Model

The five concept classes of the international release are shown on the left hand side in their three levels or groups (MP, MPF, and CD) with their two representations - the _containing_ and the _only_ - of the open and closed world views respectively. The sixth and optional class of MP Precisely is also shown, as that class may be used in a national extension model, if required.

The classes of the national extension model are, with the exception of the MP Precisely and the PCD, shown on the right hand side. Two of the classes of the national extension model mirror classes in the international model; their concepts represent the real world medicinal products available within a nation that are types of the concepts in the international release:

* The optional Real Medicinal Product (RMP) mirrors the Medicinal Product Only class and represents products marketed by a single organisation (supplier) under a single name (which may be a trade or brand name) and which contain the same set of active ingredient substances.
* The Real Clinical Drug (RCD) mirrors the Clinical Drug class and represents a product marketed by a single organisation (supplier) under a single name (which may be a trade or brand name) which contains the same set of active ingredient substances in the same strength and which is formulated within a single dose form; this class, like its partner in the international edition content, is at the core of the specification.

Then there are three classes in the national extension model that represent classes that are more specific than the classes of the international model in that they represent either a more specific abstraction of a medicinal product (the MP Precisely) or medicinal products as they are presented in the supply chain in packages for clinical/patient use in a particular country. Any subpackaging used inside a single package (for example, blister strips) and the aggregate packaging used in wholesaling and delivery, such as shrink-wraps and pallets, are excluded. The three additional package classes are:

* The optional Medicinal Product Precisely (MP Precisely) which is an abstract representation of a medicinal product based on description of only and exclusively the precise active ingredients it contains.
* The optional Real Packaged Clinical Drug (RPCD) which is a representation of a packaged product marketed by a single organisation (manufacturer or supplier) under a single name (which may be a trade or brand name) which contains one or more Real Clinical Drugs within it, in set amounts.
* The optional Packaged Clinical Drug (PCD) which is an abstract representation of the Real Packaged Clinical Drug in that it has no manufacturer or supplier information and therefore represents a package containing one or more Clinical Drugs within it, in set amounts.

All concept classes in the national extension model use the closed world view and therefore include the ingredient count attributes, because when describing the real products that are authorised for supply in a country, what is stated about them must be true, and only what is stated can be true.

No requirement has been identified to suggest that the MPF class from the international core requires a mirrored class in the national extension model.

Definitions and detailed descriptions of the extension classes are given in the sections below this model introduction.

### Implementation Options

Extensions may wish to populate and use all of the classes described in the model, or they may wish to use only a subset; it is envisaged that the clinical drug class from the international core will be foundational, as will the real clinical drug in a national extension, but all others may be considered optional for implementation.

For example,

* ```
  * Some nations may not require packaged clinical drug or real packaged clinical drug concepts if all products are licensed and used in healthcare at the real clinical drug level.
  ```
  * Conversely, if a nation licenses all its products at the real packaged clinical drug level and uses those concepts in their healthcare culture, the real clinical drug class should be populated, as it acts as a grouper concept for all the packages associated with it. This grouper concept is important particularly if extensions require additional product characteristic information, such as for excipients of concern.

Similarly, some nations may require the MP Precisely concept for some classes of medicines where the precise ingredient substance can affect the clinical characteristics such as potency (e.g., glucocorticosteroids) if these concepts need to be available to support _dose based prescribing_ (i.e., prescribing that specifies a medicine concept, plus a route of administration, a dose quantity and a dose frequency, but does not specify a dose form or a strength, so therefore not a clinical drug with its precise ingredient substance). MP Precisely concepts can be authored in a national extension.

Extensions may wish to author additional clinical drug concepts using a presentation strength description for liquid products for which the international release has only a concentration strength representation.

All authored concepts should classify correctly despite the absence of some intermediary classes, provided that they have been modeled according to the SNOMED International standards, that is using the proximal primitive parent and the relevant attributes for the concept class.

## Class Relationships

The model uses the standard generalisation/specialisation relationship between the mirrored "real" classes of the national extension and their abstract classes in the international core. It also uses a partitive relationship, shown in the diagram as the specialised composition relationship (the 'live together, die together' relationship), between the Clinical Drug and Packaged Clinical Drug classes, indicating that the Packaged Drug classes are "composed of" concepts that are themselves Clinical Drugs. This is reflected in the [774160008 | Contains clinical drug (attribute)|](http://snomed.info/id/774160008) that is part of the logical definition of a Packaged Clinical Drug. The composition relationship is particularly appropriate for those packaged medicinal products that contain more than one clinical drug (often referred to as _kit products_). The combination of the usual SNOMED CT generalisation relationship and partitive relationship is manageable within SNOMED CT tooling and will be applicable for description of other types of product concepts within the overall scope of SNOMED CT, such as medical devices, which are often composed of more than one type of entity (e.g., drug eluting stents). The use of the composition relationship between Clinical Drugs and Packaged Clinical Drugs means that if implementations wish to display Packaged Clinical Drugs with a direct relationship to the Clinical Drugs that they contain (as in "under" them in a hierarchical display), and they wish to transfer information such as the therapeutic role from the Clinical Drug to the Packaged Clinical Drug that they are related to, this composition relationship and the [774160008 | Contains clinical drug (attribute)|](http://snomed.info/id/774160008) must be used to facilitate that.

The relationships in the diagram are shown only in terms of their semantics; no cardinality is given. National extensions may populate those classes for which they have use cases; for example, if a nation has no requirement for the Real Medicinal Product class, it does not have to be populated.

## Relationship between International and Extension Content

The international core content of SNOMED CT will provide all the **attribute** **relationships** needed to define medicinal product concepts in a national extension. These will be suitably defined according to SNOMED CT Machine-Readable Concept Model (MRCM) principles and available for use in the tooling. The concepts to provide the **values** for the product name and supplier cannot be present in the International edition, as these do not have international applicability or even international uniqueness (especially for product name). This specification therefore cannot provide ranges for these attributes; the supertype concepts are available ( [774167006 | Product name (product name)|](http://snomed.info/id/774167006) and [774164004 | Supplier (supplier)|](http://snomed.info/id/774164004) ) to support extension authoring.

For various reasons, not all the individual Medicinal Product and Clinical Drug concepts that a nation requires may be present in the International edition; some additional content may require authoring in the nation's own extension. All the substance, dose form, unit of presentation, and package type concepts to value the attributes should be available in the international content to satisfy the interoperability use cases for the medicinal product hierarchy. Strengths can be described accurately using the appropriate integer or decimal, following editorial rules.

All concepts in the classes of the national extension model should be modelled using the proximal primitive parent modeling pattern and be fully defined wherever possible, using the attribute relationships and values from the international content for the substance, dose form and unit of presentation concepts and values from the national extension for product names and manufacturer/supplier organisations, but it is accepted that some primitive concepts may have to be authored.
