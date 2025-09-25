# Introduction

# Rationale for the National Drug Extension Model

The international content of SNOMED CT is, by definition, globally applicable. For example, most clinicians will agree on what constitutes a diagnosis of atrial fibrillation and how this concept should be logically defined. Therefore, wherever in the world a patient suffers from atrial fibrillation, there is a common understanding of what that is, and the SNOMED CT concept for atrial fibrillation can represent and reflect that.

But medicinal products are different. Concepts in a Medicinal Product terminology can be divided into two types:

  1. Those concepts whose representation is abstract but which can be understood and used internationally (with sufficient language support). These are described generically using their internationally recognised constituent parts, which are: 
     * Active ingredient substance(s) and basis of strength substances described (whenever possible) using their international non-proprietary names (INNs) possible
     * Active ingredient strength(s), described using international standards and principles such as the RTO<PQ> datatype (the ratio of physical quantities - see _International Organization for Standards, Health informatics — Harmonized data types for information interchange ISO 32090:2011_) and/or UCUM units of measure or their equivalent, which in SNOMED CT is accomplished by using specific attributes for each of the numerator and denominator values (represented as a concrete value) and units (represented as a SNOMED CT concept)
     * Pharmacopoeial / internationally defined dose forms
     * Pharmacopoeial / internationally defined units of presentation (when appropriate)
  2. Those concepts which describe real or actual products available for clinical use whose representation can only be fully described and understood within a jurisdiction, as they are governed by the regulations of that jurisdiction and produced by authorisation of a medicines regulatory agency responsible for that jurisdiction. This includes:
     * Authorised product names (which may be brand or trademarked names). A brand name in one jurisdiction may relate to a different product than the same brand name used in another jurisdiction (although medicines regulatory agencies are trying to reduce this because of the safety issues it raises).
     * Proprietary dose forms, including those describing a timing component (e.g. "caplets", "24-hour prolonged release tablets")
     * Additional characteristics in the product name such as
       * Inclusion or exclusion of particular excipients with various roles ("strawberry flavour", "sugar-free")
       * Target population groups ("for children")
       * Indication for use ("cough and cold")
     * Packaging information
       * pack size
       * container description

International SNOMED CT releases contain concepts of the first type, i.e., those whose representation is both understandable internationally and whose use has international applicability (e.g., in support of medication information in international patient summaries, or for international pharmacovigilance). But clinical care _within_ member nations requires both the first _and_ the second type of representation for medicinal products to enable each country to express _their_ medicinal products with _their_ names, _their_ definitions, and if required, additional defining attributes that fit with _their_ regulation and _their_ healthcare culture and practice. This national drug extension model is provided to support the authoring of drug concepts of this second type, and to enable the sharing of tools (e.g., drug authoring tools), rules (e.g., international decision support rules), and drug extension content (e.g., to support the interoperability of a patient's medication information, for cross-border dispensing with contraindication checking).

# Use Cases for the National Drug Extension Model

National drug extensions have to support a variety of use cases; these can include any or all of:

  * Prescribing medicines - such that medicinal products are described in _sufficient_ detail that the next action in the process (either dispensing or administration) can identify the correct product to dispense/administer
  * Dispensing
    * Reimbursement information
    * Supply chain management (including ordering of medicines for dispensing)
    * "Track and trace" including fraudulent medicines avoidance
  * Administration
    * Closed loop medication systems
  * Medication history/patient medication lists
  * Linking to decision support
  * Pharmacovigilance
  * Secondary uses (clinical research, pharmacoepidiemiology)
  * Supporting electronic data exchange for any or all of the above use cases (for both human users and for system users)

# Purpose

The drug extension concept model can be used to represent the real or actual medicinal products (sometimes referred to as _branded products_) available for use in a particular country/territory. This model is compatible with the international core model for Medicinal Products. This compatibility means that, when classified using the appropriate tooling, the extension concepts will be correctly placed alongside other concepts in the international Medicinal Product hierarchy. 

Detailed rules and processes required to populate a national terminology are not described here. General principles are given, and terming suggestions are provided. However, national extensions must be mindful of their own terming requirements when authoring synonyms to support direct implementation. In situations where additional concepts for core classes of the international model are required in the national extension (e.g., MP, MPF, and CD), the naming guidelines for the international release should be followed (particularly for the FSN).

General principles for authoring SNOMED CT extension content can be found in the Extensions Practical Guide at [General Authoring Principles](https://docs.snomed.org/snomed-ct-practical-guides/snomed-ct-extension-guide/5-key-steps/5.4-authoring/5.4.1-general-authoring-principles).

# Scope

The scope of this concept model (as defined) is limited to medicinal products (pharmaceutical and biological). Blood products, foods, additives, and complementary medicines (including homeopathic products) are out of scope. Vaccines are also out of scope (even though they are biological medicinal products).

National extensions will need to make decisions about the scope of their own medicinal product terminology and may require the representation of products that are beyond the international scope. In these cases, it may be necessary to author Clinical Drug concepts (and their associated MP and MPFs) within the extension (e.g., to describe national pharmacopoeial formulations). In addition, national extensions will need to set a scope for the range of medicinal products to be included. Factors to consider include:

  * Licensed medicinal products (i.e., those with a valid authorisation within the jurisdiction of the extension)
    * This may or may not include those licensed for sale or supply without an order (prescription) from a healthcare professional. These products are often known as "over the counter" medicines.
  * Unlicensed medicinal products
    * Previously licensed medicinal products - i.e. those that have, at some point, held a valid authorisation within the extension's jurisdiction, but which no longer do. Some of these previously licensed products may continue to be available (e.g., via import)
    * Medicinal products holding a valid authorisation in a **different** jurisdiction, which are (regularly) used within the extension's jurisdiction by practitioners at their own clinical discretion
    * Medicinal products that are compounded according to recognised formulae. These are usually produced by authorised compounding units.
    * Investigational medicinal products (if and when good sources of this information become available through IDMP)

In all of the above, a reliable source of information for all the definitional attributes are required. This may be challenging for unlicensed medicines and even for some "over the counter" medicines.

It can be helpful when considering the boundary for inclusion of products in the national extension (if the national prescribing use case is in scope), to include those products that can be 'legally supplied'; in most healthcare cultures, compounded products, unlicensed and investigational products can be legally supplied to patients provided the terms and conditions of the jurisdiction are fulfilled. The scope must also bear in mind how to respond to the changes in the availability of products over time and the use case(s) for historic information for products that are no longer available in the supply chain. The principles for the status of the terminology concepts themselves should be as in the core (i.e., active - intended for terminology use; inactive - not intended for terminology use). The implications of this, in terms of use cases for active supply of medicines, must also be considered.

This specification does not propose a model for the types of additional knowledge that may be a useful part of a national medicinal product catalogue, such as product availability or pricing. That is a matter for each jurisdiction. 

# Audience

This document is written primarily for those responsible for the development and maintenance of a Medicinal Product terminology (national, regional or organisational) that is managed within a SNOMED CT extension. However, it will also be of value to those who have an existing Medicinal Product terminology (national, regional or organisational) which may or may not be managed in a SNOMED CT extension, who wish to develop a mapping from concepts in their own Medicinal Product terminology to a standardized SNOMED CT representation to harness the interoperability benefits of using a common concept model defined in a clinical reference terminology.

  







<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=SCT+Editorial+Guide&entry.670899847=Introduction" class="button primary">Provide Feedback</a>
