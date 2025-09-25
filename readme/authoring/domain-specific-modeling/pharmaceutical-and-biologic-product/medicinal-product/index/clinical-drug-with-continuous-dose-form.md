# Clinical Drug with Continuous Dose Form

## Overview

Clinical drugs representing a continuous dose form are modeled using _concentration_ strength attributes. Clinical drugs with a _continuous_ dose form using _concentration_ strength represents a medicinal product based on description of 1) its precise active ingredient substances only and explicitly, 2) the stated basis of strength substance(s) with strength, expressed as concentration strength and 3) with its manufactured dose form (with the exception of reconstituted oral liquid preparations, where the administrable dose form is be used as it is the most clinically relevant).

This is used for product types such as cutaneous semi-solids (without metered actuation), solutions, suspensions, creams, ointments, bulk powders and granules, topical liquids (without metered actuation) including drops, oral liquids, nebuliser liquids and liquid parenteral products.

For example,

* Product containing precisely zidovudine 10 milligram/1 milliliter conventional release oral solution (clinical drug)
* Product containing precisely amikacin (as amikacin sulfate) 250 milligram/1 milliliter conventional release solution for injection (clinical drug)
* Product containing precisely clotrimazole 10 milligram/1 gram conventional release cutaneous cream (clinical drug)
* Product containing precisely mupirocin (as mupirocin calcium) 20 milligram/1 gram conventional release nasal ointment (clinical drug)

## Modeling

| **Stated parent**                                                                                        | 763158003 \|Medicinal product (product)\|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Semantic tag**                                                                                         | (clinical drug)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Definition status**                                                                                    | <p>Defined</p><p>Exception:</p><ul><li>Concepts with product strength that is "not equal to" (e.g. with product strength expressed as a range, greater than, or less than) are primitive</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <p><strong>Attribute:</strong></p><p><strong>Has manufactured dose form</strong></p>                     | <p>Range: 736542009 |Pharmaceutical dose form (dose form)|</p><ul><li>While the allowed range for this attribute is broader, the CD-precise continuous dose from concepts should only use &#x3C;736542009 | Pharmaceutical dose form (dose form), excluding grouper concepts based on intended site (e.g. 740596000 |Cutaneous dose form (dose form)|, 385268001 |Oral dose form (dose form)|).</li></ul><p>Cardinality: 1..1</p><p>Note</p><ul><li>This is the finished dose form that a medicinal product is presented in by the manufacturer, before any transformation into an administrable dose form has taken place.</li></ul><p>Powder and granules for oral suspension, solution, etc., may be modeled using concentration strength and the administrable dose form.</p><p>For example,</p><ul><li>1145409004 |Product containing precisely amoxicillin 25 milligram/1 milliliter and clavulanic acid (as clavulanate potassium) 6.25 milligram/1 milliliter conventional release oral suspension (clinical drug)|</li></ul> |
| <p><strong>Attribute:</strong></p><p><strong>Count of base of active ingredient (attribute)</strong></p> | <p>Concrete Type: Integer</p><p>Range: >#0..</p><p>Cardinality: 1..1</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Relationship group**                                                                                   | **One relationship group containing one instance of each of the following attributes is required for each precise active ingredient.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <ul><li><strong>Has precise active ingredient</strong></li></ul>                                         | <p>Range: &#x3C;105590001 |Substance (substance) excluding concepts representing structural groupers, dispositions, or combined substances</p><p>Cardinality: 1..1 per relationship group</p><ul><li>The Precise Active Ingredient (PAI) cannot be modeled as a substance hydrate or solvate unless the BoSS is expressed as a hydrate or solvate.</li><li>Concepts containing pancreatic enzymes will be modeled based on the discrete enzymes; because of variability between real clinical drugs, synonyms representing a total amount in a particular product will not be included in the International Release.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <ul><li><strong>Has basis of strength substance</strong></li></ul>                                       | <p>Range:  &#x3C;105590001 |Substance (substance) excluding concepts representing structural groupers, dispositions, or combined substances</p><p>Cardinality:  1..1 per relationship group</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <ul><li><strong>Has concentration strength numerator value</strong></li></ul>                            | <p>Concrete Type:  Decimal</p><p>Range:  >#0..</p><p>Cardinality:  1..1 per relationship group</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <ul><li><strong>Has concentration strength numerator unit</strong></li></ul>                             | <p>Range: &#x3C;767524001 |Unit of measure (qualifier value)|</p><p>Cardinality: 1..1 per relationship group</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <ul><li><strong>Has concentration strength denominator value</strong></li></ul>                          | <p>Concrete Type: Decimal</p><p>Range: >#0..</p><p>Cardinality: 1..1 per relationship group</p><p>For this pattern, the attribute value must be 1.</p><p>The denominator strength value is required for concepts in the International Release even though the value = 1, because including denominators for only some concepts negatively affects the classification results.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <ul><li><strong>Has concentration strength denominator unit</strong></li></ul>                           | <p>Range:  &#x3C;767524001 |Unit of measure (qualifier value)|</p><p>Cardinality:  1..1 per relationship group</p><p> </p><p>For Clinical drug concepts with:</p><ul><li>liquid dose form: the denominator unit should be 258773002 |Milliliter (qualifier value)|.</li><li><p>semi-solid dose form: the denominator unit should be</p><p><a href="http://snomed.info/id/258682000">258682000 | gram (qualifier value)|</a>for weight/weight concentration and 258773002 |Milliliter (qualifier value)| for weight/volume concentration.  Representing semi-solid dose forms in weight/weight concentration is preferred.</p></li></ul>                                                                                                                                                                                                                                                                                                                                                                                               |

## Naming

Use one of the following patterns for the FSN and PT.

### FSN

**Where Precise active ingredient = BoSS:**

* Product containing precisely \<BoSS FSN> \<Concentration strength numerator value FSN> \<Concentration strength numerator unit FSN>/\<Concentration strength denominator value FSN> \<Concentration strength denominator unit FSN> \<Manufactured dose form FSN> (clinical drug)

For example,

* Product containing precisely amitriptyline hydrochloride 5 milligram/1 milliliter conventional release oral solution (clinical drug)
* Product containing precisely buprenorphine 70 microgram/1 hour prolonged-release transdermal patch (clinical drug)
* Product containing precisely clotrimazole 10 milligram/1 gram conventional release cutaneous cream (clinical drug)
* Product containing precisely zidovudine 10 milligram/1 milliliter conventional release oral solution (clinical drug)
* Product containing precisely lopinavir 80 milligram/1 milliliter and ritonavir 20 milligram/1 milliliter conventional release oral solution (clinical drug)\


**Where Precise active ingredient is not = BoSS:**

* Product containing precisely \<BoSS FSN> (as \<Precise active ingredient FSN>) \<Concentration strength numerator value FSN> \<Concentration strength numerator unit FSN>/\<Concentration strength denominator value FSN> \<Concentration strength denominator unit FSN> \<Manufactured dose form FSN> (clinical drug)

For example,

* Product containing precisely amikacin (as amikacin sulfate) 250 milligram/1 milliliter conventional release solution for injection (clinical drug)
* Product containing precisely mupirocin (as mupirocin calcium) 20 milligram/1 gram conventional release nasal ointment (clinical drug)

### Preferred Term

**Where Single ingredient with BoSS = Precise active ingredient:**

* \<BoSS PT> \<Concentration strength numerator value PT> \<Concentration strength numerator unit PT>/\<Concentration strength denominator value PT> \<Concentration strength denominator unit PT> \<Manufactured dose form PT>

For example,

* Amitriptyline hydrochloride 5 mg/mL oral solution
* Buprenorphine 70 microgram/hour prolonged-release transdermal patch
* Clotrimazole 10 mg/g cutaneous cream
* Zidovudine 10 mg/mL oral solution
* Lopinavir 80 mg/mL and ritonavir 20 mg/mL oral solution

**Where Single ingredient with BoSS is not = Precise active ingredient:**

* \<BoSS PT> (as \<Precise active ingredient PT>) \<Concentration strength numerator value PT> \<Concentration strength numerator unit PT>/\<Concentration strength denominator value PT> \<Concentration strength denominator unit PT> \<Manufactured dose form PT>

For example,

* Amikacin (as amikacin sulfate) 250 mg/mL solution for injection
* Mupirocin (as mupirocin calcium) 20 mg/g nasal ointment

### Synonym

Synonyms converting metric units to percent or parts per millions may be included for medical gas concepts (e.g. Helium 79% and oxygen 21% gas for inhalation, Helium 790,000 ppm and oxygen 210,000 ppm gas for inhalation).

## Exemplars

### Stated template view

<figure><img src="../../../../../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

### Example Concepts

<figure><img src="../../../../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 781834001 |Product containing precisely digoxin 250 microgram/1 milliliter conventional release solution for injection (clinical drug)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (9) (1).png" alt=""><figcaption><p> <strong>Inferred</strong> view for 781834001 |Product containing precisely digoxin 250 microgram/1 milliliter conventional release solution for injection (clinical drug)|-</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (10) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 769821007 |Product containing precisely digoxin 50 microgram/1 milliliter conventional release oral solution (clinical drug)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (53) (1).png" alt=""><figcaption><p><strong>Inferred</strong> view for 769821007 |Product containing precisely digoxin 50 microgram/1 milliliter conventional release oral solution (clinical drug)|.</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (54) (1).png" alt=""><figcaption><p><strong>Stated</strong> view for 396279000 |Product containing precisely betamethasone (as betamethasone valerate) 1 milligram/1 gram conventional release cutaneous ointment (clinical drug)|.</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (55).png" alt=""><figcaption><p><strong>Inferred</strong> view for 396279000 |Product containing precisely betamethasone (as betamethasone valerate) 1 milligram/1 gram conventional release cutaneous ointment (clinical drug)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (56).png" alt=""><figcaption><p><strong>Stated</strong> view for 769514000 |Product containing precisely buprenorphine 70 microgram/1 hour prolonged-release transdermal patch (clinical drug)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (57).png" alt=""><figcaption><p><strong>Inferred</strong> view for 769514000 |Product containing precisely buprenorphine 70 microgram/1 hour prolonged-release transdermal patch (clinical drug)|.</p></figcaption></figure>

<figure><img src="../../../../../../authoring/pharmaceutical-and-biologic-product/images/174690867.png" alt=""><figcaption></figcaption></figure>
