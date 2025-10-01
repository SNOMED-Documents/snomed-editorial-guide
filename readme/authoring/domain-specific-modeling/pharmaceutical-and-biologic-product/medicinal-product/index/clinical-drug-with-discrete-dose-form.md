# Clinical Drug with Discrete Dose Form

## Overview

Clinical drug concepts representing discrete dose form (e.g., tablets, capsules, pessaries, suppositories, sachets, patches, ampules or vials containing solid dose forms such as powders or granules, and metered dose delivery products such as inhalers and spray) are modeled using _presentation_ strength attributes; concentration strength attributes are not allowed for these concepts in the International Release. Clinical drugs with a discrete dose form using presentation strength represents a medicinal product based on description of 1) its precise active ingredient substances only and explicitly, 2) the stated basis of strength substance(s) with strength, expressed as presentation strength with unit of presentation and 3) with its manufactured dose form.

For example,

* Product containing precisely abacavir 300 milligram/1 each conventional release oral tablet (clinical drug)
* Product containing precisely abacavir 600 milligram and lamivudine 300 milligram/1 each conventional release oral tablet (clinical drug)
* Product containing precisely afatinib (as afatinib dimaleate) 30 milligram/1 each conventional release oral tablet (clinical drug)
* Product containing precisely aztreonam 500 milligram/1 vial powder for conventional release solution for injection (clinical drug)
* Product containing precisely flucloxacillin (as flucloxacillin sodium) 250 milligram/1 vial powder for conventional release solution for injection (clinical drug)
* Product containing precisely budesonide 200 microgram/1 actuation conventional release powder for inhalation (clinical drug)
* Product containing precisely nicotine 7 milligram/24 hour prolonged-release transdermal patch (clinical drug)

{% hint style="warning" %}
#### Exception

Pre-filled pens or cartridges are discrete dose forms as they can be counted. In the International edition of SNOMED CT, clinical drugs presenting in pre-filled pens or cartridges are modeled with normalized _concentration strength_.

Example of pre-filled pen:

* One pre-filled pen for injection contains 2 mg semaglutide in a 1.5 ml solution
* FSN: 782102009 |Product containing precisely semaglutide 1.34 milligram/1 milliliter conventional release solution for injection (clinical drug)|
{% endhint %}

When a product has a metered delivery, the strength is "per actuation" not as a concentration.

> For example
>
> 1263426000 |Product containing precisely xylometazoline hydrochloride 140 microgram/1 actuation conventional release nasal spray (clinical drug)|

{% hint style="danger" %}
Lyophilized dose forms are out of scope for the international edition of SNOMED CT.
{% endhint %}

## Modeling

<table data-header-hidden><thead><tr><th width="374"></th><th></th></tr></thead><tbody><tr><td><strong>Stated parent</strong></td><td><code>763158003 |Medicinal product (product)</code></td></tr><tr><td><strong>Semantic tag</strong></td><td>(clinical drug)</td></tr><tr><td><strong>Definition status</strong></td><td><p>Defined</p><ul><li><p>Exception:</p><ul><li>Concepts with product strength that is "not equal to" (e.g. with product strength expressed as a range, greater than, or less than) will have a definition status of Primitive.</li></ul></li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Has manufactured dose form</p></td><td><p><strong>Range:</strong> <code>&#x3C;736542009 |Pharmaceutical dose form (dose form)</code></p><p></p><ul><li>While the allowed range for this attribute is broader, the CD-precise<br>discrete dose form concepts should only use <code>&#x3C;736542009 |Pharmaceutical dose form (dose form)|</code>, excluding grouper concepts based on intended site (e.g. <code>740596000 |Cutaneous dose form (dose form)|</code>, <code>385268001 |Oral dose form (dose form)|</code>)</li></ul><p></p><p><strong>Cardinality:</strong> 1..1</p><p></p><p>Powder and granules for oral suspension, solution, etc. may be modeled using<br>concentration strength and the administrable dose form (e.g. <code>1145409004 |Product</code><br><code>containing precisely amoxicillin 25 milligram/1 milliliter and clavulanic acid (as clavulanate</code><br><code>potassium) 6.25 milligram/1 milliliter conventional release oral suspension (clinical drug)|</code>)</p></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Has unit of presentation</p></td><td><p><strong>Range:</strong> <code>&#x3C;732935002 |Unit of presentation (unit of presentation)|</code> </p><p></p><p><strong>Cardinality:</strong> 1..1 </p><p></p><p><strong>Note:</strong>  </p><ul><li>This is the countable entity in which the clinical drug is presented </li></ul><ul><li>See <a href="../../pharmaceutical-and-biologic-product-and-dose-form-attributes-summary/appendix-a-product-patterns/"><em>Appendix A: Product Patterns</em></a> for the various patterns of use for the unit of presentation</li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p>Count of base of active ingredient (attribute)</p></td><td><p><strong>Concrete Type:</strong> Integer</p><p><strong>Range:</strong> >#0..</p><p><strong>Cardinality:</strong> 1..1</p></td></tr><tr><td><strong>Relationship group</strong></td><td><strong>One relationship group containing one instance of each of the following attributes is required for each precise active ingredient.</strong></td></tr><tr><td><p><strong>Attribute</strong>:</p><p>Has precise active ingredient</p></td><td><p><strong>Range:</strong> <code>&#x3C;105590001 |Substance (substance)|</code> excluding concepts representing structural groupers, dispositions, or combined substances </p><p></p><p><strong>Cardinality:</strong> 1..1 per relationship group </p><p></p><p><strong>Note</strong>: </p><ul><li>The PAI cannot be modeled as a substance hydrate or solvate unless the BoSS is expressed as a hydrate or solvate. </li></ul><ul><li>Concepts containing pancreatic enzymes are modeled based on the discrete enzymes; because of variability between real clinical drugs, synonyms representing a total amount in a particular product will not be included in the International Release.</li></ul></td></tr><tr><td><p><strong>Attribute</strong>:</p><p>Has basis of strength substance</p></td><td><p><strong>Range</strong>: <code>&#x3C;105590001 |Substance (substance)|</code> excluding concepts representing structural groupers, dispositions, or combined substances</p><p></p><p><strong>Cardinality</strong>: 1..1 per relationship group</p></td></tr><tr><td><strong>Attribute</strong>:<br>Has presentation strength numerator value</td><td><p><strong>Concrete Type</strong>: Decimal</p><p></p><p><strong>Range:</strong> >#0..</p><p></p><p><strong>Cardinality</strong>: 1..1 per relationship group</p></td></tr><tr><td><strong>Attribute</strong>:<br>Has presentation strength numerator unit</td><td><p><strong>Range</strong>: <code>&#x3C;767524001 |Unit of measure (qualifier value)|</code> </p><p></p><p>Cardinality: 1..1 per relationship group</p></td></tr><tr><td><strong>Attribute</strong>:<br>Has presentation strength denominator value</td><td><p><strong>Concrete Type</strong>: Decimal</p><p></p><p><strong>Range</strong>: >#0..</p><p></p><p><strong>Cardinality</strong>: 1..1 per relationship group</p><p>For this pattern, the attribute value is 1.</p><p></p><p>The denominator strength value is required for concepts in the International Release, even if the value = 1, because including denominators for only some concepts negatively affects the classification results.</p></td></tr><tr><td><strong>Attribute:</strong><br>Has presentation strength denominator unit</td><td><p><strong>Range</strong>: <code>&#x3C;767524001 |Unit of measure (qualifier value)|</code> </p><ul><li>While the allowed range for this attribute is broader, the CD-precise concepts representing discrete dose forms should only use <code>&#x3C;732935002 |Unit of presentation (unit of presentation)</code>. </li></ul><p></p><p><strong>Cardinality</strong>: 1..1 per relationship group</p></td></tr></tbody></table>

## Naming

Use one of the following patterns for the FSN and PT.

### FSN

**Where Precise active ingredient = BoSS and Unit of presentation = discrete solid dose form (e.g. capsule, lozenge, pessary, suppository, tablet):**

Product containing precisely \<BoSS FSN> \<Presentation strength numerator value FSN> \<Presentation strength numerator unit FSN>/\<Presentation strength denominator value FSN> each \<Manufactured dose form FSN> (clinical drug)

* For example,
  * Product containing precisely abacavir 300 milligram/1 each conventional release oral tablet (clinical drug)
  * Product containing precisely abacavir 600 milligram and lamivudine 300 milligram/1 each conventional release oral tablet (clinical drug)
  * Product containing precisely atropine sulfate 600 microgram/1 each conventional release oral tablet (clinical drug)
  * Product containing precisely codeine sulfate 15 milligram/1 each conventional release oral tablet (clinical drug)

**Where Precise active ingredient is not = BoSS and Unit of presentation = discrete solid dose form (e.g. capsule, lozenge, pessary, suppository, tablet):**

Product containing precisely \<BoSS FSN> (as \<Precise active ingredient FSN>) \<Presentation strength numerator value FSN> \<Presentation strength numerator unit FSN>/\<Presentation strength denominator value FSN> each \<Manufactured dose form FSN> (clinical drug)

* For example,
  * Product containing precisely doxazosin (as doxazosin mesilate) 4 milligram/1 each conventional release oral tablet (clinical drug)
  * Product containing precisely disopyramide (as disopyramide phosphate) 150 milligram/1 each prolonged-release oral tablet (clinical drug)

**Where Precise active ingredient = BoSS and Unit of presentation = other discrete dose form (e.g. actuation, vial, sachet)**

Product containing precisely \<BoSS FSN> \<Presentation strength numerator value FSN> \<Presentation strength numerator unit FSN>/Presentation strength denominator value FSN> \<Presentation strength denominator unit FSN> Manufactured dose form FSN> (clinical drug)

* For example,
  * Product containing precisely aztreonam 500 milligram/1 vial powder for conventional release solution for injection (clinical drug)
  * Product containing precisely budesonide 200 microgram/1 actuation conventional release powder for inhalation (clinical drug)

**Where Precise active ingredient is not = BoSS and Unit of presentation = other discrete dose form (e.g. actuation, vial, sachet)**

Product containing precisely \<BoSS FSN> (as \<Precise active ingredient FSN>) \<Presentation strength numerator value FSN> \<Presentation strength numerator unit FSN>/\<Presentation strength denominator value FSN> \<Presentation strength denominator unit FSN> Manufactured dose form FSN> (clinical drug)

* For example,
  * Product containing precisely flucloxacillin (as flucloxacillin sodium) 250 milligram/1 vial powder for conventional release solution for injection (clinical drug)
  * Product containing precisely buserelin (as buserelin acetate) 100 microgram/1 actuation conventional release nasal spray (clinical drug)

### Preferred Term

**Where BoSS = Precise active ingredient:**

* \<BoSS PT> \<Presentation strength numerator value PT> \<Presentation strength numerator unit PT> \<Manufactured dose form PT> \<Has unit of presentation PT>

For example,

* Abacavir 300 mg oral tablet
* Abacavir 600 mg and lamivudine 300 mg oral tablet
* Atropine sulfate 600 microgram oral tablet
* Codeine sulfate 15 mg oral tablet
* Aztreonam 500 mg powder for solution for injection vial
* Budesonide 200 microgram/actuation powder for inhalation
* Buserelin (as buserelin acetate) 100 microgram/actuation nasal spray
* Ivacaftor 25 mg oral granules sachet

**Where BoSS is not = Precise active ingredient:**

* \<BoSS PT> (as \<Precise active ingredient PT>) \<Presentation strength numerator value PT> \<Presentation strength numerator unit PT> \<Manufactured dose form PT> \<Has unit of presentation PT>

For example,

* US PT: Doxazosin (as doxazosin mesylate) 4 mg oral tablet
* GB PT: Doxazosin (as doxazosin mesylate) 4 mg oral tablet
* US/GB PT: Disopyramide (as disopyramide phosphate) 150 mg prolonged-release oral tablet
* US PT: Floxacillin (as floxacillin sodium) 250 mg powder for solution for injection vial
* GB PT: Flucloxacillin (as flucloxacillin sodium) 250 mg powder for solution for injection vial

### Synonym

Synonyms matching the FSN are not required.

## Exemplars

### Stated Template View

<figure><img src="../../../../../../.gitbook/assets/image (54).png" alt=""><figcaption><p>Template</p></figcaption></figure>

### Example Concepts

<figure><img src="../../../../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 318783003 |Product containing precisely doxazosin (as doxazosin mesilate) 4 milligram/1 each conventional release oral tablet (clinical drug)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 318783003 |Product containing precisely doxazosin (as doxazosin mesilate) 4 milligram/1 each conventional release oral tablet (clinical drug)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 783301004 |Product containing precisely abacavir (as abacavir sulfate) 600 milligram and lamivudine 300 milligram/1 each conventional release oral tablet (clinical drug)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 783301004 |Product containing precisely abacavir (as abacavir sulfate) 600 milligram and lamivudine 300 milligram/1 each conventional release oral tablet (clinical drug)|</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690776.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Clinical%20Drug%20with%20Discrete%20Dose%20Form" class="button primary">Provide Feedback</a>
