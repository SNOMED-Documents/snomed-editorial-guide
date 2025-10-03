# Pharmaceutical Dose Form Naming and Modeling Conventions

## Overview

Pharmaceutical dose form concepts (e.g. conventional release oral tablet, prolonged-release oral capsule) that are deemed to be clinically useful and that can be sufficiently defined will be included in the 736542009 |Pharmaceutical dose form (dose form)| hierarchy. Primitive concepts may be included if documented as an exception.

### Out of Scope

Lyophilized dose forms are out of scope for the international edition of SNOMED CT.

## Modeling

<table data-header-hidden><thead><tr><th width="211.50390625"></th><th></th></tr></thead><tbody><tr><td><strong>Semantic tag</strong></td><td>(dose form)</td></tr><tr><td><strong>Definition status</strong></td><td><p>Defined</p><p><strong>Exceptions</strong>:</p><ul><li><p>The following referenced in concepts cannot be sufficiently defined.  They are modeled with a parent of <code>736542009 |Pharmaceutical dose form (dose form)</code> with all applicable attributes and have a Definition status of <em>Primitive</em>. </p><ul><li>coated</li><li>drug delivery system</li><li>iontophoresis (e.g. <code>385113008 |Conventional release solution for iontophoresis (dose form)|</code>)</li><li>nebulizer (e.g. <code>385198000 |Conventional release solution for nebulizer (dose form)|</code>)</li><li>particle (<code>421535006 |Gastro-resistant oral particles tablet (dose form)|</code>)</li><li>pellet (e.g. <code>420767002 |Gastro-resistant oral pellets capsule (dose form)|</code>)</li><li>syrup (e.g. <code>385033009 |Powder for conventional release oral syrup (dose form)|</code>)</li><li>vapor</li></ul></li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Has basic dose form</p></td><td><p><strong>Range</strong>:  <code>&#x3C;736478001 |Basic dose form (basic dose form)|</code></p><p><strong>Cardinality</strong>: 0..1</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one and only one |Has basic dose form| attribute.</li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Has dose form intended site</p></td><td><p><strong>Range</strong>:  <code>&#x3C;736479009 |Dose form intended site (intended site)|</code></p><p><strong>Cardinality</strong>: 0..*</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one or more |Has dose form intended site| attributes.<br></li></ul><p><strong>Exceptions</strong>:</p><ul><li><code>785898006 |Conventional release solution for irrigation (dose form)|</code></li><li><code>785910004 |Prolonged-release intralesional implant (dose form)|</code></li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Has dose form release characteristic<br></p></td><td><p><strong>Range</strong>:  <code>&#x3C;736480007 |Dose form release characteristic (release characteristic)|</code><br></p><p><strong>Cardinality</strong>: 0..1</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one and only one |Has dose form release characteristic| attribute.</li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Has dose form administration method</p></td><td><p><strong>Range</strong>:  <code>&#x3C;736665006 |Dose form administration method (administration method)|</code></p><p><strong>Cardinality</strong>: 0..*</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one and only one |Has dose form administration method| attribute.</li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Has dose form transformation</p></td><td><p><strong>Range</strong>: <code>&#x3C;736477006 |Dose form transformation (transformation)|</code></p><p><strong>Cardinality</strong>: 0..*</p><ul><li>While the allowed range is broader, concepts representing a sufficiently defined pharmaceutical dose form should have one and only one |Has dose form transformation| attribute. </li></ul></td></tr></tbody></table>

## Naming

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

Use the following pattern for the PT; align naming and case sensitivity with the PT for the concepts that are selected as the attribute values, excluding the semantic tag. For multiple intended sites, the sites must be in alphabetical order and separated by the word “and”. Exclude \<Dose form release characteristic> when = `736849007 |Conventional release (release characteristic)|`.

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

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Pharmaceutical%20Dose%20Form%20Naming%20and%20Modeling%20Conventions" class="button primary">Provide Feedback</a>
