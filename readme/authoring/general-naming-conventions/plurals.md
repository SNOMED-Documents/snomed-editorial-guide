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

# Plurals

## Fully specified names (FSNs) <a href="#fully-specified-names-fsns" id="fully-specified-names-fsns"></a>

In general, concepts are represented in the singular, rather than the plural.

* For example:
  * |Disorder of lung (disorder)|, not |Disorder of lungs|
  * |Acute cholecystitis due to biliary calculus (disorder)|, not |Acute cholecystitis due to biliary calculi (disorder)

FSNs should not be plural unless the concept necessarily involves multiples.

## Unintended plurals <a href="#unintended-plurals" id="unintended-plurals"></a>

_Unintended plurals_ might be incorrectly interpreted. An unintended plural is the use of a plural when, in fact, there is only one entity.

* Correct example:
  * _Multiple cranial nerve palsies_; the word _multiple_ indicates that there can never be just one, so the plural _palsies_ is correct
* Incorrect example:&#x20;
  * _Trochlear lesion_ versus _trochlear lesions;_ users would use this concept to refer to a single trochlear lesion, thus the plural form would be incorrect

## Exceptions <a href="#exceptions" id="exceptions"></a>

Organizational nodes or grouper concepts may be plural.&#x20;

* For example,
  * [234320004 | Procedures for splenic lesions (procedure)|](http://snomed.info/id/234320004)
  * [194732001 | Diseases of mitral and aortic valves (disorder)|](http://snomed.info/id/194732001), has IS A [195002007 | Multiple valve disease (disorder)|](http://snomed.info/id/195002007)

A concept that necessarily involves multiples should have a plural FSN.&#x20;

* For example,
  * Bilateral atrophy of testes (disorder)

{% hint style="warning" %}
It is advisable to keep track of these exceptions in a separate subset or using a special term type, so that they can be excluded when the singular/plural distinction is important for mapping.
{% endhint %}
