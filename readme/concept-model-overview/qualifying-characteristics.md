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

# Qualifying Characteristics

A _qualifying characteristic_ is expressed by an attribute-value pair. The attribute may have one value, from a range of values, based on the domain's concept model. If a particular qualifying characteristic is applied to a concept, the resulting expression represents a more tightly defined subtype of that concept.

{% hint style="info" %}
Clinical expressions using SNOMED CT concepts can be of two types: precoordinated expressions, which use a single SNOMED CT concept identifier; and postcoordinated expressions, which contain more than one SNOMED CT concept identifier.
{% endhint %}

For example,

*   It might be possible to qualify a disorder such as

    [53084003 | Bacterial pneumonia (disorder)|](http://snomed.info/id/53084003) according to its clinical course ([373933003 | Acute onset (qualifier value)|](http://snomed.info/id/373933003) or [90734009 | Chronic (qualifier value)|](http://snomed.info/id/90734009)) or severity ([255604002 | Mild (qualifier value)|](http://snomed.info/id/255604002), [6736007 | Moderate (severity modifier) (qualifier value)|](http://snomed.info/id/6736007), or [24484000 | Severe (severity modifier) (qualifier value)|](http://snomed.info/id/24484000))
* [125605004 | Fracture of bone (disorder)|](http://snomed.info/id/125605004) can be refined by qualifying it with [12611008 | Bone structure of tibia (body structure)|](http://snomed.info/id/12611008) to represent the concept [31978002 | Fracture of tibia (disorder)|](http://snomed.info/id/31978002)
