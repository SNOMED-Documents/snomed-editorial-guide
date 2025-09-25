# Pharmaceutical Dose Form Naming and Modeling Conventions

## Overview

Pharmaceutical dose form concepts (e.g. conventional release oral tablet, prolonged-release oral capsule) that are deemed to be clinically useful and that can be sufficiently defined will be included in the 736542009 |Pharmaceutical dose form (dose form)| hierarchy. Primitive concepts may be included if documented as an exception.

### Out of Scope

Lyophilized dose forms are out of scope for the international edition of SNOMED CT.

## Modeling

| **Parent concept**                                                                                     | 736542009 \|Pharmaceutical dose form (dose form)\|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Semantic tag**                                                                                       | (dose form)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Definition status**                                                                                  | <p>Defined</p><p>Exceptions:</p><ul><li><p>The following referenced in concepts cannot be sufficiently defined.  They are modeled with a parent of 736542009 |Pharmaceutical dose form (dose form) with all applicable attributes and have a Definition status of <em>Primitive</em>. </p><ul><li>coated</li><li>drug delivery system</li><li>iontophoresis (e.g. 385113008 |Conventional release solution for iontophoresis (dose form)|)</li><li>nebulizer (e.g. 385198000 |Conventional release solution for nebulizer (dose form)|)</li><li>particle (421535006 |Gastro-resistant oral particles tablet (dose form)|)</li><li>pellet (e.g. 420767002 |Gastro-resistant oral pellets capsule (dose form)|)</li><li>syrup (e.g. 385033009 |Powder for conventional release oral syrup (dose form)|)</li><li>vapor</li></ul></li></ul> |
| <p><strong>Attribute:</strong></p><p><strong>Has basic dose form</strong></p>                          | <p>Range:  &#x3C;736478001 |Basic dose form (basic dose form)|</p><p>Cardinality: 0..1</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one and only one |Has basic dose form| attribute.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <p><strong>Attribute:</strong></p><p><strong>Has dose form intended site</strong></p>                  | <p>Range:  &#x3C;736479009 |Dose form intended site (intended site)|</p><p>Cardinality: 0..*</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one or more |Has dose form intended site| attributes.</li></ul><p>Exceptions:</p><ul><li>785898006 |Conventional release solution for irrigation (dose form)|</li><li>785910004 |Prolonged-release intralesional implant (dose form)|</li></ul>                                                                                                                                                                                                                                                                                                                                                           |
| <p><strong>Attribute:</strong></p><p><strong>Has dose form release characteristic</strong><br><br></p> | <p>Range:  &#x3C;736480007 |Dose form release characteristic (release characteristic)|</p><p>Cardinality: 0..1</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one and only one |Has dose form release characteristic| attribute.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <p><strong>Attribute:</strong></p><p><strong>Has dose form administration method</strong></p>          | <p>Range:  &#x3C;736665006 |Dose form administration method (administration method)|</p><p>Cardinality: 0..*</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one and only one |Has dose form administration method| attribute.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p><strong>Attribute:</strong></p><p><strong>Has dose form transformation</strong></p>                 | <p>Range:  &#x3C;736477006 |Dose form transformation (transformation)|</p><p>Cardinality: 0..*</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one and only one |Has dose form transformation| attribute. </li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

## Terming

### FSN

Use the following pattern for the FSN; align naming and case sensitivity with the FSN for the concepts that are selected as the attribute values, excluding the semantic tag. For multiple intended sites, the sites must be in alphabetical order and separated by the word “and”.

\<Dose form release characteristic FSN> \<Dose form intended site FSN> \<Basic dose form> (dose form)

For example,

* Conventional release oral capsule (dose form)
* Conventional release oral suspension (dose form)
* Prolonged-release oral capsule (dose form)
* Conventional release and prolonged-release oral tablet (dose form)
* Conventional release cutaneous cream (dose form)
* Conventional release vaginal ointment (dose form)
* Gastro-resistant oral suspension (dose form)

### Preferred Term

Use the following pattern for the PT; align naming and case sensitivity with the PT for the concepts that are selected as the attribute values, excluding the semantic tag. For multiple intended sites, the sites must be in alphabetical order and separated by the word “and”. Exclude \<Dose form release characteristic> when = 736849007 |Conventional release (release characteristic)|.

\<Dose form release characteristic FSN> \<Dose form intended site FSN> \<Basic dose form>

For example,

* Oral capsule
* Oral suspension
* Prolonged-release oral capsule
* Conventional release and prolonged-release oral tablet
* Cutaneous cream
* Vaginal ointment
* Gastro-resistant oral suspension

### Synonym

A synonym matching the FSN is required; other synonyms are not allowed unless explicitly identified as an exception in the Editorial Guidelines.

Exceptions:

* Synonyms with _eye_ instead of _ocular_, _ear_ instead of _otic_, or _nose_ instead of _nasal_ may be created.

### Text Definition

Optional

## Exemplar

<figure><img src="../../../../../../.gitbook/assets/image (72).png" alt=""><figcaption><p><strong>Stated</strong> view for 385024007 |Conventional release oral suspension (dose form)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (73).png" alt=""><figcaption><p><strong>Inferred</strong> view for 385024007 |Conventional release oral suspension (dose form)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (74).png" alt=""><figcaption><p><strong>Stated</strong> view for 764774009 |Conventional release and prolonged-release oral tablet (dose form)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (75).png" alt=""><figcaption><p><em><strong>Inferred</strong></em> view for 764774009 |Conventional release and prolonged-release oral tablet (dose form)|</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174691246.png" alt=""><figcaption></figcaption></figure>
