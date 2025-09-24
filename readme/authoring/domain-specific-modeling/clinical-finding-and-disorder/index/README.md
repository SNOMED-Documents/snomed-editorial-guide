# Clinical Finding and Disorder Naming Conventions

## Clinical Finding and Disorder Naming Conventions

A Clinical finding/Disorder concept's fully specified name (FSN) must be specific, though the preferred term (PT) can be a more clinician-friendly, word-order variant.

## FSN

### FSN Pattern

The FSN must conform to a specific pattern of "Disease of x" where a specific body structure is involved. For the preferred term, end users can choose the desired description that conforms to common clinical usage.

For example,

* FSN: Disease of kidney (disorder)
* PT: Can be either 'Kidney disease' or 'Renal disease'

### Use of -_opathy_

The use of -_opathy_ is to be used in the preferred term, because the FSN is to be specific and explicit, and there are often various interpretations of -_opathy_. A term containing the suffix -opathy can only be used in the FSN if a definition is applied via the DEF description.

For example,

* FSN: Disorder of macula of retina (disorder)
* PT: Can be either 'Disorder of macula of retina' or 'Maculopathy'

### Order of site and morphology

The morphologic abnormality is named before naming the anatomical site.

For example,

* In 399525009 | Inflammation of ampulla of Vater (disorder)|, **Inflammation** is the morphologic abnormality and **Ampulla of Vater** is the finding site.

{% hint style="warning" %}
**Exceptions**

While the general naming convention for findings and disorders is _< Morphology> of_ , there are some exceptions:

* Disorders with a well recognized name that represents the morphology; e.g. pneumonia is the well established clinical name for inflammation and infection of the lung
* Disorders where the meaning is not equivalent to _< morphology> of_ site convention; e.g. _inflammatory bowel disease_ has a more specific meaning than _inflammation of bowel_
* Disorders which are not described by an anatomical site; e.g. metabolic disease, hereditary disease, bacterial disease
* Completed or in review - [Pre-coordination Naming Patterns Project](https://prod-confluence.ihtsdotools.org/display/IHTSDO1/Pre-coordination+Naming+Patterns+Project)
* Proposed for future review - [Unreviewed Patterns by Hierarchy](https://prod-confluence.ihtsdotools.org/display/IHTSDO1/Unreviewed+Patterns+by+Hierarchy)
{% endhint %}

### Descriptions that include body structures

Descriptions for Clinical findings and Disorders should follow the naming guidelines for Body structures if they are to be used within the Clinical finding/disorder concept.

Concepts describing limbs are abundant, and the use of _limb_ in the FSN and the synonyms of upper/lower extremity, arm/leg should be followed.

For example,

* [249945007 |Monoparesis of lower limb (disorder)|](http://snomed.info/id/249945007)

Because the finding site is 61685007 |Lower limb structure (body structure)|, which follows the anatomical guidelines, the disorder concept reflects _lower limb_ in the FSN, while using synonyms of _Monoparesis of leg_ and _Monoparesis of lower extremity_.

The term _cerebral_ is used in clinical language to mean both _cerebrum_ , and more broadly, _brain_.

* If the condition is limited to the cerebrum, the FSN, PT, and finding site will reflect the cerebrum. A synonym will remain with the term _cerebral_.
* If the condition refers more broadly to the brain, the FSN, PT, and finding site will reflect the brain – unless the proper name of the condition uses the term _cerebral_ , as in _Cerebral palsy_. A synonym will remain with the term _cerebral_ if it is commonly used to refer to the condition.

### The term Disorder

The word _disorder_ should be singular, so _Disorder of nose_ , not _Disorders of nose_.

Plurals may be used:

* As synonyms for grouper concepts, e.g. _disorders_ or _diseases_
* In bilateral concepts, e.g. Disorder of bilateral eyes, Disorder of both eyes (see also _Lateralized Disorder Naming Conventions_)
* When the concept is a general grouping of disorders of a body system, body site, or other broad category, the word _disorder_ is preferred over the word _disease_ for the FSN, e.g. _Disorder of reproductive system_ , not _Disease of reproductive system_. This does not apply at the leaf level.

For example,

* [417683006 | Sickle cell-hemoglobin C disease without crisis (disorder)|](http://snomed.info/id/417683006)

For naming conventions concerning _surgical complications, sequelae, and late effects;_ see this section at [Complication and Sequela Modeling](../clinical-finding-and-disorder-modeling/complication-and-sequela-modeling.md).

### Disorder X without Disorder Y

The vast majority of existing X without Y concepts originated from ICD-9 with the specific meaning of "X disorder _without mention_ of Y disorder". As the phraseology indicates a lack of data about disorder Y as opposed to a specific exclusion, this type of concept has not been included in ICD-10, nor proposed for ICD-11, except in the case of "Traumatic brain injury without open intracranial wound".

Addition of new X without Y concepts may only be made under the following conditions:

* The request for new content must be accompanied by a rationale as to the difference between "X disorder without Y disorder" and "X disorder"
* Approval of addition by the Chief Terminologist

For the most part, existing _X without Y_ concepts will be inactivated as AMBIGUOUS with a historical MAY BE relationship to "X disorder". Exceptions to inactivation will be made on a case-by-case basis.

### Requires \[procedure/drug] (finding)

SNOMED international is no longer accepting new requests for concepts of the type – Requires \[procedure/drug] (finding). These are administrative statuses rather than clinical findings, and this status should be represented outside of the terminology in the information model. The only exceptions relate to legacy content, and requests for subtypes of 723620004 |Requires vaccination (finding)| will continue to be accepted.

## Region

If the [363698007 | Finding site (attribute)|](http://snomed.info/id/363698007) value of a concept is a body structure with "region" in its FSN, then the description of the finding site within the clinical finding concept's FSN should also include "region".

For example, [274205003 | Burn of eye region (disorder)|](http://snomed.info/id/274205003) has a finding site of [371398005 | Eye region structure (body structure)|](http://snomed.info/id/371398005) .

* FSN: Burn of eye region (disorder)
* PT: Burn of eye region

<figure><img src="../../../../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Figure 1. Stated view of |Burn of eye region (disorder)|</p></figcaption></figure>

## Allergy to substances, multiple substances

Previously, allergies caused by multiple substances were modeled by multiple causative agents suggesting that the allergy is caused by all those substances. However, when multiple substances are noted in the FSN, the intended clinical meaning is that a patient might be affected by one or more of these substances (or products containing them). To convey this meaning, these types of concepts should be modeled GCIs to represent the disjunctive meaning. e.g. 870731003 |Allergy to carbidopa and/or levodopa (finding)|

{% hint style="info" %}
The modeling approach for multiple-ingredient concepts is a temporary solution. It incorrectly asserts an allergy/adverse reaction to each, rather than to one, agent. The use of concepts from the Pharmaceutical/biologic product hierarchy is being considered as a final solution, but further work is required to determine if this would be a viable solution.
{% endhint %}

## Allergic and nonallergic hypersensitivity (pseudoallergic) _dispositions_

Allergic and nonallergic hypersensitivity (pseudoallergic) dispositions are the propensity to develop adverse allergic or nonallergic hypersensitivity (pseudoallergic) disorders. A description for any concept that names a substance or an organism should be consistent with the corresponding hierarchy description rules.

{% hint style="warning" %}
**Drug allergies**\


Allergic and nonallergic hypersensitivity (pseudoallergic) concepts include drug allergies.
{% endhint %}

### Pattern - Allergy to single substance:

* FSN: Allergy to X (finding)
* PT: Allergy to X

For example,

* FSN: Allergy to abacavir (finding)
* PT: Allergy to abacavir
* FSN: Allergy to Artemisia vulgaris pollen (finding)
* PT: Allergy to mugwort pollen

### Pattern - Allergy to multiple substances:

FSN: Allergy to X and Y (finding)

PT: Allergy to X and Y

* X and Y in alphabetical order for concepts representing multiple substances

## Allergic and nonallergic hypersensitivity (pseudoallergic) _disorders_

These disorders represent manifestations of pathologic processes that may result in abnormal structures (e.g., allergic rhinitis).

<table><thead><tr><th width="169.73828125">Disorder</th><th>Patterns and examples</th></tr></thead><tbody><tr><td>FSN</td><td><p>Patterns:</p><ul><li>FSN: Allergic disease X (disorder)</li><li>FSN: Allergic disease X (caused by Y) (disorder)</li></ul><p>For example,</p><ul><li>Allergic rhinitis (disorder)</li><li>Allergic conjunctivitis (disorder)</li><li>Allergic rhinitis caused by grass pollen (disorder)</li><li>Allergic rhinitis caused by house dust mite (disorder)</li></ul></td></tr><tr><td>PT</td><td><p>Patterns:</p><ul><li>Allergic disease X</li><li>Allergic disease X (caused by Y)</li></ul><p>For example,</p><ul><li>Allergic rhinitis</li><li>Allergic conjunctivitis</li><li>Allergic rhinitis caused by grass pollen</li><li>Allergic rhinitis caused by house dust mite</li></ul></td></tr></tbody></table>

## Allergic and nonallergic hypersensitivity (pseudoallergic) _reactions_

These disorders represent pathological processes that are defined as adverse reactions and allergic conditions with a pathological process of allergic or nonallergic hypersensitivity (pseudoallergic) process.

<table><thead><tr><th width="132.0859375">Reaction</th><th>Patterns and examples</th></tr></thead><tbody><tr><td>FSN</td><td><p>Patterns:</p><ul><li>Allergic reaction (caused by X) (disorder)<br></li><li>Anaphylactic reaction (caused by X) (disorder)</li><li>Anaphylactoid reaction (caused by X) (disorder)</li></ul><p>For example, </p><ul><li>Allergic reaction caused by dye (disorder)</li><li>Allergic reaction caused by pollen (disorder)</li></ul></td></tr><tr><td>PT</td><td><p>Patterns: </p><ul><li>Allergic reaction caused by X</li></ul><p>For example,</p><ul><li>Allergic reaction caused by dye</li><li>Allergic reaction caused by pollen</li></ul></td></tr></tbody></table>

## Contact hypersensitivity

Contact hypersensitivity represents a response elicited by contact of the skin or mucous membranes with a substance. The response may be immune mediated (allergic) or nonimmune (irritant) using the pathological process _c_ _ontact hypersensitivity process (qualifier value)._

For example,

* Contact dermatitis (disorder)
* Irritant contact dermatitis (disorder)

## Intolerance to substances

An intolerance is the propensity to develop an adverse reaction to a substance. The nature of the adverse reaction can represent a variety of pathological processes but specifically excludes hypersensitivity (allergic and nonallergic hypersensitivity (pseudoallergic) reactions.

Due to the difficulty in precisely defining an intolerance pathological process, it is problematic to apply the model for hypersensitivity dispositions to defining intolerance to substance. For this reason, as well as the difficulty in associating a material agent with a disposition, substances are related to the intolerance disposition with the _associated with_ attribute.

<table><thead><tr><th width="173.26171875">Intolerance</th><th>Patterns and examples</th></tr></thead><tbody><tr><td>FSN</td><td><p>Pattern:</p><ul><li>Intolerance to X (finding)</li></ul><p>Example,</p><ul><li>Intolerance to milk (finding)</li></ul></td></tr><tr><td>PT</td><td><p>Pattern:</p><ul><li>Intolerance to X</li></ul><p>Example,</p><ul><li>Intolerance to milk</li></ul></td></tr></tbody></table>

## Inadequate and excessive intake of energy and nutrients

Identification of findings of inadequate or excessive intake of nutrients inconsistent with nutrient requirements and established reference standards includes nutrients with a variety of forms where applicable.

For example, [870465001 | Excessive intake of vitamin A and vitamin A derivative (finding)|](http://snomed.info/id/870465001)

* FSN: Excessive intake of vitamin A and vitamin A derivative (finding)
* PT: Excessive intake of vitamin A and vitamin A derivative
