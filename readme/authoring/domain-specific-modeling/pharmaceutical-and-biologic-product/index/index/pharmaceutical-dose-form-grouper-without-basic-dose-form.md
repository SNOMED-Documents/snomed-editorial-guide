# Pharmaceutical Dose Form Grouper Without Basic Dose Form

## Overview

Pharmaceutical dose form grouper concepts that do not include a basic dose form but are deemed to be clinically useful and that can be sufficiently defined will be included in the 736542009 |Pharmaceutical dose form (dose form)| hierarchy.

## Modeling

Grouper concepts concepts that do not include a basic dose form shall be modeled using the proximal primitive modeling pattern.

| **Parent concept**                                                                             | 736542009 \|Pharmaceutical dose form (dose form)                                                                                                |
| ---------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Semantic tag**                                                                               | (dose form)                                                                                                                                     |
| **Definition status**                                                                          | <p>Defined</p><p>Exception:</p><ul><li>Grouper concepts representing drug delivery systems will have a definition status of Primitive</li></ul> |
| <p><strong>Attribute:</strong></p><p><strong>Has dose form release characteristic</strong></p> | Range: << 736480007                                                                                                                             |
| <p><strong>Attribute:</strong></p><p><strong>Has dose form intended site</strong></p>          | Range: << 736479009                                                                                                                             |
| <p><strong>Attribute:</strong></p><p><strong>Has dose form administration method</strong></p>  | Range: << 736665006                                                                                                                             |

## Naming

### FSN

For concepts with 736472000 |Has dose form administration method (attribute)| = 738996007 |Spray (administration method)|, use the following pattern for the FSN; align naming and case sensitivity with the FSN for the concept that is selected as the attribute value. For multiple intended sites, the intended sites must be in alphabetical order and separated by the word “and”.

* \<Dose form release characteristic> \<Dose form intended site FSN> \<Dose form administration method> (dose form)

For example,

* Conventional release cutaneous spray (dose form)
* Conventional release nasal spray (dose form)
* Conventional release sublingual spray (dose form)

***

For concepts representing drops with 736472000 |Has dose form administration method (attribute)| = 738994005 |Instill (administration method)|, use the following pattern for the FSN; align naming and case sensitivity with the FSN for the concept that is selected as the attribute value. For multiple intended sites, the intended sites must be in alphabetical order and separated by the word “and”.

* \<Dose form release characteristic> \<Dose form intended site FSN> \<Dose form administration method> (dose form)

For example,

* Conventional release nasal drops (dose form)
* Prolonged-release eye drops (dose form)

***

For concepts representing drug delivery systems, use the following pattern for the FSN; align naming and case sensitivity with the FSN for the concept that is selected as the attribute value. For multiple intended sites, the intended sites must be in alphabetical order and separated by the word “and”.

* \<Dose form release characteristic> \<Dose form intended site FSN> drug delivery system

For example,

* Prolonged-release intrauterine drug delivery system (dose form)
* Prolonged-release transdermal drug delivery system (dose form)

### Preferred Term

For concepts with 736472000 |Has dose form administration method (attribute)| = 738996007 |Spray (administration method)|, use the following pattern for the PT; align naming and case sensitivity with the PT for the concept that is selected as the attribute value. For multiple intended sites, the intended sites must be in alphabetical order and separated by the word “and”. Exclude \<Dose form release characteristic> when = 736849007 |Conventional release (release characteristic)|.

* \<Dose form release characteristic> \<Dose form intended site FSN> \<Dose form administration method>

For example,

* Cutaneous spray
* Nasal spray
* Sublingual spray

***

For concepts representing drops with 736472000 |Has dose form administration method (attribute)| = 738994005 |Instill (administration method)|, use the following pattern for the PT; align naming and case sensitivity with the PT for the concept that is selected as the attribute value. For multiple intended sites, the intended sites must be in alphabetical order and separated by the word “and”. Exclude \<Dose form release characteristic> when = 736849007 |Conventional release (release characteristic)|.

* \<Dose form release characteristic> \<Dose form intended site FSN> \<Dose form administration method>

For example,

* Nasal drops
* Prolonged-release eye drops

***

For concepts representing drug delivery systems, use the following pattern for the PT; align naming and case sensitivity with the PT for the concept that is selected as the attribute value. For multiple intended sites, the intended sites must be in alphabetical order and separated by the word “and”. Exclude \<Dose form release characteristic> when = 736849007 |Conventional release (release characteristic)|.

* \<Dose form release characteristic> \<Dose form intended site FSN> drug delivery system

For example,

* Prolonged-release intrauterine drug delivery system (dose form)
* Prolonged-release transdermal drug delivery system (dose form)

### Synonym

A synonym matching the FSN is required; additional synonyms are not allowed unless explicitly identified as an exception in the Editorial Guidelines.

Exceptions:

* Synonyms with _eye_ instead of _ocular_, _ear_ instead of _otic_, or _nose_ instead of _nasal_ may be created.

### Text Definitions

Optional

## Exemplars

<figure><img src="../../../../../../.gitbook/assets/image (77).png" alt=""><figcaption><p>S<strong>tated</strong> view for concept 385105007 |Conventional release cutaneous spray (dose form)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (78).png" alt=""><figcaption><p>I<strong>nferred</strong> view for concept 385105007 |Conventional release cutaneous spray (dose form)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (79).png" alt=""><figcaption><p><strong>Stated</strong> view for concept 385152001 |Conventional release nasal drops (dose form)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (83).png" alt=""><figcaption><p>I<strong>nferred</strong> view for concept 385152001 |Conventional release nasal drops (dose form)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (80).png" alt=""><figcaption><p><strong>Stated</strong> view for concept 421716009 |Prolonged-release transdermal drug delivery system (dose form)|:</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (82).png" alt=""><figcaption><p><strong>inferred</strong> view for concept 421716009 |Prolonged-release transdermal drug delivery system (dose form)|</p></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Pharmaceutical%20Dose%20Form%20Grouper%20Without%20Basic%20Dose%20Form" class="button primary">Provide Feedback</a>
