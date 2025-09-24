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

# Domain Specific Modeling

SNOMED CT is arranged as a polyhierarchy. A _hierarchy_ is defined as an ordered organization of concept codes linked together through IS A relationships. Concept codes are linked to their more general parent concept codes directly above them in a hierarchy. Concepts with more general meanings are usually located at the top of the hierarchy and then at each level down the hierarchy the meanings become increasingly more specialized.

Selected SNOMED CT attributes have a hierarchical relationship to one another known as _attribute hierarchies_. In an attribute hierarchy, one general attribute is the parent of one or more specific subtypes of that attribute. Concepts defined using the more general attribute can inherit concepts modeled with the more specialized subtypes of that attribute.

Domains

The following are the 19 domains arranged in alphabetical order.

* [Body Structure](body-structure/)
* [Clinical Finding and Disorder](clinical-finding-and-disorder/)
* [Environment and Geographical Location](environment-and-geographical-location.md)
* [Event](event/)
* [Observable Entity](observable-entity/)
* [Organism](organism/)
* [Pharmaceutical and Biologic Product](pharmaceutical-and-biologic-product/)
* [Physical Force](physical-force.md)
* [Physical Object](physical-object/)
* [Procedure](procedure/)
* [Qualifier Value](qualifier-value/)
* [Record Artifact](record-artifact.md)
* [Situation with Explicit Context](situation-with-explicit-context/)
* [SNOMED CT Model Component](snomed-ct-model-component.md)
* Social Context
* [Special Concept](special-concept.md)
* [Specimen](../../../Specimen_174691394.html)
* [Staging and Scales](staging-and-scales.md)
* [Substance](substance/)

The following subhierarchies do not have concept models:

* Environment or geographical location (environment / location)
* Organism (organism)
* Physical force (physical force)
* Qualifier value (qualifier value)
* Record artifact (record artifact)
* SNOMED CT Model Component (metadata)
* Social context (social concept)
* Special concept (special concept)
* Staging and scales (staging scale)

## MRCM Attribute Tables

The pages that follow contain tables that are generated from the Machine Readable Concept Model (MRCM). The tables contain Attribute Summaries for those domains with attributes, information on _Group(ed)_, _Cardinality_, and _In-group cardinality_, and Range constraints. The MRCM tables in this guide only reflect the ranges for pre-coordinated concepts; there may be post-coordination values that are not reflected in the tables. All MRCM values for concepts can be viewed via the public MRCM browser at [https://browser.ihtsdotools.org/mrcm](https://browser.ihtsdotools.org/mrcm).

SNOMED International creates precoordinated content in accordance with the MRCM. For postcoordinated content, extensions should review the MRCM. If the MRCM does not specify that a particular value is allowed for a given content type (e.g., using an observable entity value for |Component| in a postcoordinated expression), then it must not be used in that content type (e.g., postcoordinated expressions). The MRCM rules for postcoordination must be strictly followed. This is important for interoperability, being able to query the resulting content consistently, etc. However, the MRCM does provide the option for extensions to extend or adapt the rules in a controlled way if required (see the last section of [6. Considerations](https://prod-confluence.ihtsdotools.org/display/DOCMRCM/6.+Considerations)). This includes expanding the ranges and/or adding new attributes where required. This needs to be done carefully to ensure consistency and data integrity between editions.

There are special cases in the MRCM where an attribute may have two rows. This situation is caused by a new cardinality rule: a row for _existing/legacy_ SNOMED CT content and a row for _newly created_ content. The row that is applicable to _new_ content will be marked by a "\[New]" notation.

See [Process for the maintenance of MRCM rules](https://conf.spaces.snomed.org/wiki/spaces/IAP/pages/132481260/Process+for+the+maintenance+of+MRCM+rules).

SNOMED CT relies on the rules for _usefulness_ to avoid excessive precoordination (see _Scope_ section of Editorial Guide).

Approved precoordination patterns have been created and are available at: [Pre-coordination Naming Patterns Project](https://conf.spaces.snomed.org/wiki/spaces/IHTSDO1/pages/130978180/Pre-coordination+Naming+Patterns+Project). For additional information about the fields used in precoordination, see: [What the fields in the Pre-coordination Naming Patterns JIRA Project mean](https://conf.spaces.snomed.org/wiki/spaces/IHTSDO1/pages/130991902/What+the+fields+in+the+Pre-coordination+Pattern+JIRA+Project+mean).
