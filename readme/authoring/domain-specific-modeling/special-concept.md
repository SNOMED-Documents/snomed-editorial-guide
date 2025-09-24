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

# Special Concept

| Definition                            | Examples                                                                                                                     |
| ------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Inactive concept Navigational concept | 363664003 \| Erroneous concept (inactive concept) \| 394899003 \| Oral administration of treatment (navigational concept) \| |

## Inactive concepts

_Inactive concepts_ are no longer active in the terminology. When the first release format (RF1) was used, inactivated content was moved into this hierarchy. However, this approach is no longer used in the current release format (RF2).

## Navigational concepts

The concepts in navigational hierarchies are used for structured data entry and support the location of concepts in hierarchies. They can order data by priority or another convention (e.g. _cranial nerve order_ or _topics related to diabetes_). Navigational concepts exist only to support navigation.

NO LONGER SUPPORTED IN SNOMED CT CORE

Navigational concepts:

* Are not suitable for recording or aggregating information
* Are direct subtypes of the concept [363743006 | Navigational concept (navigational concept)|](http://snomed.info/id/363743006)
* Have no other supertype or subtype relationships
* Are linked to other concepts only by navigational links

For more information on navigational concepts, [click here](../general-modeling/grouper-concept.md).
