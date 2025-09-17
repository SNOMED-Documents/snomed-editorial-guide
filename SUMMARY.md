# Table of contents

* [SNOMED CT Editorial Guide](snomed-ct-editorial-guide.md)

* [SNOMED CT Introduction](introduction/index.md)
  * [SNOMED CT Introduction](introduction/snomed-ct-introduction.md)
  * [What is SNOMED CT?](snomed-ct-introduction.md)
  * [Why use SNOMED CT?](snomed-ct-introduction.md)
  * [Intended Use](introduction/intended-use.md)
  * [Structure of Domain Coverage](introduction/structure-of-domain-coverage.md)
  * [Granularity](structure-of-domain-coverage.md)
  * [Knowledge Representation](introduction/knowledge-representation.md)
  * [Out of Scope](introduction/out-of-scope.md)
    * National and local extensions
    * Veterinary extension
    * Classification-derived phrases
    * Regulatory or legal status
    * Funding care delivery
  * [SNOMED CT Requirements](introduction/snomed-ct-requirements.md)
    * [Medical Vocabularies - J. Cimino](introduction/medical-vocabularies-j-cimino.md)
    * [Electronic Health Applications](introduction/electronic-health-applications.md)
    * [Implementation and Migration](introduction/implementation-and-migration.md)
    * [User Communities](introduction/user-communities.md)
    * [Summary of SNOMED CT Requirements](introduction/summary-of-snomed-ct-requirements.md)

* [Concept Model Overview](concept-model-overview/index.md)
  * [Concept Model Overview](concept-model-overview/concept-model-overview.md)
  * [Root and Top-level Concepts](concept-model-overview/root-and-top-level-concepts.md)
  * [Attributes](concept-model-overview/attributes.md)
  * [Defining Characteristics](concept-model-overview/defining-characteristics.md)
  * [Qualifying Characteristics](concept-model-overview/qualifying-characteristics.md)

* [Authoring](authoring/index.md)
  * [Authoring](authoring/authoring.md)
  * [Modeling philosophy of SNOMED CT](authoring/authoring.md)
  * [Advantages of the approach](authoring/authoring.md)
  * [Content that does not conform](authoring/authoring.md)
  * [Authoring information](authoring/authoring.md)
  * [Scope](authoring/scope.md)
    * [Adjudication for Content Requests](authoring/adjudication-for-content-requests.md)
    * [Proprietary Names and Works](authoring/proprietary-names-and-works.md)
  * [General Naming Conventions](authoring/general-naming-conventions.md)
    * [Descriptions](authoring/descriptions.md)
      * [Fully Specified Name](authoring/fully-specified-name.md)
      * [Preferred Term](authoring/preferred-term.md)
      * [Synonym](authoring/synonym.md)
      * [Definition](authoring/definition.md)
    * [Case Significance](authoring/case-significance.md)
    * [Person Naming Conventions](authoring/person-naming-conventions.md)
      * Patient vs Subject
      * Caregiver vs Carer
    * [Plurals](authoring/plurals.md)
    * [Punctuation and Symbols](authoring/punctuation-and-symbols.md)
    * [Sentence Types](authoring/sentence-types.md)
    * [US vs. GB English](authoring/us-vs-gb-english.md)
      * Principles for selecting preferred spelling variants
      * Fetal vs. Foetal
    * [Action Verbs](authoring/action-verbs.md)
      * Past tense
    * [Numbers and Numeric Ranges](authoring/numbers-and-numeric-ranges.md)
      * Roman numerals versus Arabic numbers
      * Numeric ranges
  * [General Modeling](authoring/general-modeling.md)
    * [Annotations](authoring/annotations.md)
      * Use case
      * Guidance
    * [Changes to Components](authoring/changes-to-components.md)
      * Description Inactivation
      * Concept Inactivation
    * [Conjunction and Disjunction](authoring/conjunction-and-disjunction.md)
    * [General Concept Inclusions - GCIs](authoring/general-concept-inclusions-gcis.md)
    * [Grouper Concept](authoring/grouper-concept.md)
    * [Intermediate Primitive Concept Modeling](authoring/intermediate-primitive-concept-modeling.md)
    * [Proximal Primitive Modeling](authoring/proximal-primitive-modeling.md)
      * Multiple potential primitive supertype concepts
      * GCI-Modeled primitive supertypes
    * [Relationship Group](authoring/relationship-group.md)
      * Impact of relationship grouping on inheritance
      * Same attributes in separate relationship groups
      * Procedure hierarchy
      * Clinical Finding/Disorder hierarchy
      * Situation with Explicit Context hierarchy
      * Observable Entity hierarchy
    * [Sufficiently Defined vs Primitive Concept](authoring/sufficiently-defined-vs-primitive-concept.md)
      * Sufficiently defined
      * Primitive
    * [Templates](authoring/templates.md)
  * [Domain Specific Modeling](authoring/domain-specific-modeling.md)
    * [Body Structure](authoring/body-structure/body-structure.md)
      * [Body Structure Attributes Summary](authoring/body-structure/body-structure-attributes-summary.md)
      * [Anatomical Concept Model](authoring/body-structure/anatomical-concept-model.md)
      * [Anatomical Structure Naming Conventions](authoring/body-structure/anatomical-structure-naming-conventions.md)
      * [Anatomical Structure Modeling](authoring/body-structure/anatomical-structure-modeling.md)
      * [Morphologic Abnormality Modeling](authoring/body-structure/morphologic-abnormality-modeling.md)
    * [Clinical Finding and Disorder](authoring/clinical-finding-and-disorder/clinical-finding-and-disorder.md)
      * [Clinical Finding Attributes Summary](authoring/clinical-finding-and-disorder/clinical-finding-attributes-summary.md)
      * [Clinical Finding Defining Attributes](authoring/clinical-finding-and-disorder/clinical-finding-defining-attributes.md)
      * [Clinical Finding and Disorder Naming Conventions](authoring/clinical-finding-and-disorder/clinical-finding-and-disorder-naming-conventions.md)
      * [Clinical finding and Disorder Modeling](authoring/clinical-finding-and-disorder/clinical-finding-and-disorder-modeling.md)
    * [Environment and Geographical Location](authoring/environment-and-geographical-location/environment-and-geographical-location.md)
    * [Event](authoring/event/event.md)
      * [Event Attributes Summary](authoring/event/event-attributes-summary.md)
      * [Event Modeling](authoring/event/event-modeling.md)
    * [Observable Entity](authoring/observable-entity/observable-entity.md)
      * [Observable Entity Attributes Summary](authoring/observable-entity/observable-entity-attributes-summary.md)
      * [Observable Entity Defining Attributes](authoring/observable-entity/observable-entity-defining-attributes.md)
      * [Observable Entity Naming Conventions](authoring/observable-entity/observable-entity-naming-conventions.md)
      * [Observable Entity Modeling](authoring/observable-entity/observable-entity-modeling.md)
    * [Organism](authoring/organism/organism.md)
      * [Organism Naming Conventions](authoring/organism/organism-naming-conventions.md)
    * [Pharmaceutical and Biologic Product](authoring/pharmaceutical-and-biologic-product/pharmaceutical-and-biologic-product.md)
      * [Pharmaceutical and Biologic Product and Dose Form Attributes Summary](authoring/pharmaceutical-and-biologic-product/pharmaceutical-and-biologic-product-and-dose-form-attributes-summary.md)
      * [Glossary for Medicinal Product](authoring/pharmaceutical-and-biologic-product/glossary-for-medicinal-product.md)
      * [Qualifier values supporting Pharmaceutical and Biologic Product](authoring/pharmaceutical-and-biologic-product/qualifier-values-supporting-pharmaceutical-and-biologic-product.md)
    * [Physical Force](authoring/physical-force/physical-force.md)
    * [Physical Object](authoring/physical-object/physical-object.md)
      * [Out of scope](authoring/physical-object/physical-object.md)
      * [Physical Object Attributes Summary](authoring/physical-object/physical-object-attributes-summary.md)
      * [Physical Object Defining Attributes](authoring/physical-object/physical-object-defining-attributes.md)
      * [Physical Object Naming and Modeling Conventions](authoring/physical-object/physical-object-naming-and-modeling-conventions.md)
    * [Procedure](authoring/procedure/procedure.md)
      * [Procedure Attributes Summary](authoring/procedure/procedure-attributes-summary.md)
      * [Procedure Defining Attributes](authoring/procedure/procedure-defining-attributes.md)
      * [Procedure Naming Conventions](authoring/procedure/procedure-naming-conventions.md)
      * [Procedure Modeling](authoring/procedure/procedure-modeling.md)
    * [Qualifier Value](authoring/qualifier-value/qualifier-value.md)
      * [Disposition](authoring/qualifier-value/disposition.md)
      * [International System of Units - derived unit of volume](authoring/qualifier-value/international-system-of-units-derived-unit-of-volume.md)
      * [International System of Units - unit of mass](authoring/qualifier-value/international-system-of-units-unit-of-mass.md)
      * [Technique](authoring/qualifier-value/technique.md)
    * [Record Artifact](authoring/record-artifact/record-artifact.md)
    * [Situation with Explicit Context](authoring/situation-with-explicit-context/situation-with-explicit-context.md)
      * [Situation with Explicit Context Attributes Summary](authoring/situation-with-explicit-context/situation-with-explicit-context-attributes-summary.md)
      * [Situation with Explicit Context Defining Attributes](authoring/situation-with-explicit-context/situation-with-explicit-context-defining-attributes.md)
      * [Situation with Explicit Context Naming Conventions](authoring/situation-with-explicit-context/situation-with-explicit-context-naming-conventions.md)
      * [Situation with Explicit Context Modeling](authoring/situation-with-explicit-context/situation-with-explicit-context-modeling.md)
    * [SNOMED CT Model Component](authoring/snomed-ct-model-component/snomed-ct-model-component.md)
    * [Special Concept](authoring/special-concept/special-concept.md)
      * Inactive concepts
      * Navigational concepts
    * [Specimen](authoring/specimen/specimen.md)
      * Specimen not sample in FSN
      * Combined specimens and pooled specimens
      * [Specimen Attributes Summary](authoring/specimen/specimen-attributes-summary.md)
      * [Specimen Defining Attributes](authoring/specimen/specimen-defining-attributes.md)
    * [Staging and Scales](authoring/staging-and-scales/staging-and-scales.md)
      * Assessment scale requests
      * Modeling
    * [Substance](authoring/substance/substance.md)
      * [Substance Attribute Summary](authoring/substance/substance-attribute-summary.md)
      * [Substance Defining Attributes](authoring/substance/substance-defining-attributes.md)
      * [Substance Naming and Modeling Conventions](authoring/substance/substance-naming-and-modeling-conventions.md)

* [Editorial Guide Style and Terms](editorial-guide-style-and-terms/index.md)

* [PDFs for Download](pdfs-for-download.md)
