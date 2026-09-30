---
layout:
  width: default
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
    visible: false
  tags:
    visible: true
  actions:
    visible: true
  anchors:
    visible: true
---

# Attributes

## Attribute Constructs

### Attribute

| Definition                                                                            | Notes                                                                                                                                                    | Example                             |
| ------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| Represents a characteristic of the meaning of a concept or the nature of a refinement | An attribute has a name which is represented by a concept. All of the concepts that can be used to name attributes are subtypes of the concept 410662002 | Concept model attribute (attribute) |

### Range

| Definition                                                                                                                                                          | Note                                                                                                                                                                                                                                                                                                                               | Example              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| A constrained set of values that the Concept Model permits to be applied to a specific attribute when that attribute is applied to a concept in a particular domain | <p>The range of permitted values that can be applied to an attribute is typically defined to include concepts in one or more branches of the subtype hierarchy.</p><p>The range for an attribute may include intensional or extensional definitions or both. An example of a range with an intensional definition is 370130000</p> | Property (attribute) |

Not all hierarchies in SNOMED CT have defining attributes. Many attributes apply to top-level domain hierarchies, some to more than one. Some attributes to a lower-level, or a more specific, domain hierarchy. Primitive concepts in some hierarchies may be attribute values in top-level hierarchies.

## Attribute definitions

New attributes should include a text definition clearly indicating what the attribute means in the context of SNOMED CT.

## Attribute naming

Attributes should be named to clearly communicate the property they specify and should refer to only one distinct property. The meaning of the attribute should not change if new values are added to the range.\
If a new attribute is needed, look at existing unapproved SNOMED CT attributes and as well as other ontologies to see if a suitable attribute exists, including Basic Formal Ontology (BFO) ([https://basic-formal-ontology.org](https://basic-formal-ontology.org/)), Relations Ontology (RO) ([http://www.obofoundry.org/ontology/ro.html](http://www.obofoundry.org/ontology/ro.html)), and Gene Ontology (GO) ([http://geneontology.org/](http://geneontology.org/)) as example ontologies to review.

Attributes should be named as verb senses, so that object-attribute-value relationships may actually be read. For example, a name of "Has filling (attribute)" is preferred over "Filling (attribute)" and "Has property (attribute)" is preferred over "Property (attribute)." Then a concept such as 464376000 |Saline-filled breast implant (physical object)| could be defined with the attribute "Has filling (attribute)" and a value of 387390002 |Sodium chloride (substance)|.

## Attribute datatype

Many of the attributes in SNOMED CT have a range that includes SCTIDs as an allowed value. Attributes which have a binary (e.g., Boolean) value shall be valued using a descendant of 1119301001 |Boolean value (qualifier value)|: 31874001 |True (qualifier value)|; 64100000 |False (qualifier value)|. In the July 2021 release, a new attribute was created which uses Boolean style value: 1148965004 |Is sterile (attribute)|.

## Attribute hierarchy

Selected SNOMED CT attributes have a hierarchical relationship to one another known as _attribute hierarchies_. In an attribute hierarchy, one general attribute is the parent of one or more specific subtypes of that attribute. Concepts defined using the more general attribute can inherit concepts modeled with the more specific subtypes of that attribute providing the attribute value is the same or a subtype of the attribute value used for the concept that is defined with the more general attribute.

#### Clinical finding and Event attribute hierarchies

* Associated with
  * Causative agent
  * Due to
  * Temporally related to
    * After
    * Before
    * During

#### Procedure attribute hierarchies

* Procedure Site
  * Procedure site - Direct
  * Procedure site - Indirect
* Procedure device
  * Direct device
  * Indirect device
  * Using device
    * Using access device
* Procedure morphology
  * Direct morphology
  * Indirect morphology

#### Body structure attribute hierarchy

* All or part of
  * Proper part of
    * Constitutional part of
    * Regional part of
      * Lateral half of
    * Systemic part of

#### Medicinal product attribute hierarchy

* Has ingredient (not used in the international edition)
  * Has active ingredient
  * Has precise active ingredient

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Attributes" class="button primary">Provide Feedback</a>
