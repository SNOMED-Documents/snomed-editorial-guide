# Fully Specified Name

## Definition and Purpose

| Fully specified name (FSN) definition                                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| A term unique among active descriptions in SNOMED CT that provides the meaning of a concept in a manner that is intended to be unambiguous and stable across multiple contexts. |

{% hint style="warning" %}
**Precoordinated patterns**\
For information on acceptable precoordinated naming patterns, see the [_Pre-coordination Naming Patterns project_](https://conf.spaces.snomed.org/wiki/spaces/IHTSDO1/pages/130978180)_._  New content should conform with the naming patterns; however, legacy content may not yet be updated.
{% endhint %}

An FSN is one type of description, unique among active descriptions in SNOMED CT. It provides the meaning of a concept so that it is unambiguous, stable across multiple contexts, and optimally understandable to those whose first language is not English.  Consequently, it is not always clinician-friendly or in common use.  In the majority of cases, where the FSN is clinician-friendly and in common use, a description matching the FSN should be added to the concept. This description is not required to be the preferred term (PT). In certain instances, where the FSN does not provide a clinically useful description, a matching description without the semantic tag is unnecessary.

* For example,
  * FSN: Repair of common bile duct (procedure) - _the meaning_
  * PT: Choledochoplasty - _commonly understood clinical name_

Choledochoplasty is marked as _preferred_ in the US English Language _Reference_ _Set;_ choledochoplasty is the _preferred term_ for this _concept_ in US English.&#x20;

Each new content request should have an FSN that conforms to spelling, language, and style guidelines. It should also have SNOMED CT parent concepts that conform to editorial guidelines and show where in the hierarchy it belongs. In the Content Request System (CRS), if the meaning of the FSN is unclear or the parent codes are not provided, authors should request the information from the submitter.

A well formed FSN includes:

* Correct US spelling, not GB (General British) spelling&#x20;
* Singular form, not plural form
* Procedures in present tense, not past tense
* A semantic tag in parentheses at the end

An FSN with an approved disjunctive (although not often used), e.g., |Traumatic and/or non-traumatic injury of back (disorder)| should have lower case _and/or_.&#x20;

An FSN should not have:

* Abbreviations or acronyms
  * For more information, including exceptions, see the _Abbreviations and acronyms_ section at [General Naming Conventions](https://conf.spaces.snomed.org/wiki/spaces/DOCEG/pages/133137126)
* Hyphens
* Duplicate concepts
* Ambiguity
* The word OR (exception for the disjunctive _and/or_)
* Forward or backslash (/ \\)
* Precoordinated numeric ranges
* Reference to a particular instance
* Reason or indication for a procedure, unless this directly impacts the method

{% hint style="warning" %}
Exceptions that should not be amended include:



* Trademark names
* Latin names of organism
* Scientific names
{% endhint %}

{% hint style="info" %}
**Structure, Structure of**

When constructing the FSN for a disorder, finding, or procedure containing a body structure, the wording of the body structure should follow the naming convention of the body structure concept. However, it should not include the words _structure_ or _structure of._&#x20;

* For example,&#x20;
  *   For the body structure concept, &#x20;

      [266005 | Structure of lower lobe of right lung (body structure)|](http://snomed.info/id/266005), a procedure with this body structure is [726425007 | Lobectomy of lower lobe of right lung (procedure)|](http://snomed.info/id/726425007).
  *   For the body structure concept,&#x20;

      [74386004 | Nasal bone structure (body structure)|](http://snomed.info/id/74386004), a disorder concept with this body structure is [413878002 | Closed, displaced fracture of nasal bone (disorder)|](http://snomed.info/id/413878002).
{% endhint %}

## Unique <a href="#unique" id="unique"></a>

The FSN is unique among active concepts. The SNOMED International Authoring Platform automatically creates a matching description to the FSN. Authors then determine the clinical usefulness of a synonym that matches the FSN. Those that are useful are maintained in SNOMED CT; those that are not useful are removed. The Authoring Platform displays a warning when the matching description is removed; however, this does not prevent the author from saving the concept.

The FSN should provide a linguistic representation of the concept in an unambiguous way. It is considered an anchor for the representation of meaning of a concept, to which modelers can refer, when assigning a logic-based definition. The FSN does not necessarily follow the usual phrasing used in clinical practice; it may be phrased differently and may be longer and more fully spelled out in order to represent the meaning as clearly as possible and globally communicate the intended meaning of the concept.

The characters comprising the description, as well as case significance, must be taken into account to provide for a unique FSN.  Uniqueness maintained through case sensitivity is handled by Case Significance.  It is possible to alter the semantics of concepts whose FSN uniqueness depends upon case significance. &#x20;

* For example,&#x20;
  * 38194003 |Weak e phenotype (finding)|
  * 6800004 |Weak E phenotype (finding)|

The two referenced concepts above could easily be mistaken for duplicates if not for varying case sensitivity indicators that demarcate each concept's uniqueness. &#x20;

## Unambiguous <a href="#unambiguous" id="unambiguous"></a>

A single term may have more than one meaning. Therefore, FSNs should be checked for ambiguity.

* For example, _immunosuppression_ may mean the state of being immunosuppressed, or it may mean the application procedure of immunosuppressive therapy.

The following FSNs are clear and acceptable.

* For example,
  * Benign neoplasm of clavicle (disorder)
  * Excision of cyst of spleen (procedure)

The following FSNs are ambiguous, and the concept should be inactivated.

* For example,&#x20;
  * Standing in water side toward (finding); does not indicate _which side of what is toward what_
  * Lumbar ache - renal (finding); does not convey whether the lumbar ache is specifically a renal etiology or is merely located in the renal area

## Changes to FSN <a href="#changes-to-fsn" id="changes-to-fsn"></a>

#### Minor Changes - Only the FSN changes but not the concept <a href="#minor-changes-only-the-fsn-changes-but-not-the-concept" id="minor-changes-only-the-fsn-changes-but-not-the-concept"></a>

Minor changes to an FSN are allowed without inactivation of the concept.  When making a minor change to an FSN, a new description must be created and the old description must be inactivated.  While the description ID will change, the concept ID remains the same.  FSN changes cannot change the meaning of the FSN.  Minor changes include:

* Changing case; i.e., capitalizing, or changing from upper to lower case
* Changing punctuation
* Changing spelling
* Replacing an acronym with its expansion (only if it is commonly understood and not ambiguous)
* Expanding an abbreviation
* Correcting word order without changing the meaning (only for an error)
* Correcting typos
* Removing articles, such as '_the'_
* Where a change to the FSN does not result in a change to the preferred term
* Aligning with editorial policy, e.g., changing _appendectomy_ to _excision of appendix\*_

_**\*Updating an FSN to align with editorial policy**_

Where an active concept requires an update to the FSN to conform to current editorial guidance, this may result in duplication with the FSN on an inactive concept.&#x20;

In this scenario:

* The current active concept should be retained. There is no requirement to inactivate the currently active concept and reactivate the inactive concept.
* For the concept that is inactive, the inactivation reason should be updated to ‘Duplicate’ and the association type ‘SAME\_AS’ to the active concept with the same FSN.

For example,&#x20;

Concept 27215002 had an FSN of Uterine inversion (disorder).  Editorial policy instructs this to be formatted as Inversion of uterus (disorder).  However, an inactive concept of 156232008 |Inversion of uterus (disorder)| already exists with that FSN.  156232008 |Inversion of uterus| is named correctly but has been inactive since 2002. In this case, the concept 27215002 should remain active with its FSN updated. &#x20;

The inactive concept, 156232008 |Inversion of uterus|, should be checked to ensure its inactivation reason is ‘Duplicate’ and the Association type ‘SAME\_AS’ to the active concept 27215002 with the same FSN.

{% hint style="info" %}
For circumstances where a new concept duplicates an inactive concept with the same FSN, the inactive concept should be reactivated rather than adding a new concept.
{% endhint %}

Some FSN changes are necessary for style consistency; again, changes are only acceptable if the meaning does not change.

They may include changing:

* Semantic tag type within a single top-level hierarchy\*
* For example,
  * A _finding_ tag to a _disorder_ tag
  * A _procedure_ tag to a _regime/therapy_ tag

\*When changing a concept's semantic tag within the same top-level hierarchy, use the description inactivation reason of _Non-conformance to editorial policy_.

* Changing a concept's semantic tag to _navigational concept_
* A substance or product name to reflect the International Nonproprietary Name (INN)
* The current scientific name of an organism (only applies to 410607006 |Organism (organism)| hierarchy)

#### Major Changes - When to inactivate the concept  <a href="#major-changes-when-to-inactivate-the-concept" id="major-changes-when-to-inactivate-the-concept"></a>

Major changes to FSNs require inactivation of the concept.

* The following are examples of major changes, when:
  * Changing the FSN changes the meaning
  * FSN is ambiguous
  * FSN meaning is more specific than the modeling; inactivation is determined case-by-case as this could simply be a primitive concept which cannot be defined
  * Moving to a different top-level hierarchy
    * Exception: Concept inactivation is not required for moving a concept to the _navigational concept_ hierarchy.&#x20;
  * Changing the common name to the scientific name
  * Ancestors and descendants (if any) of the concept are inconsistent with what is implied by the FSN - inactivate concepts

## International FSNs <a href="#international-fsns" id="international-fsns"></a>

The FSN for a concept in the International Release is designated an _International FSN_. The International FSN is considered the _gold standard_ for interpretation of the meaning of the concept, from a linguistic standpoint.

The logical definitions, represented using the concept model, should represent the same meaning. Spelling of the International FSN follows United States (US) English spelling conventions. Other English language spelling and conventions, such as Great Britain (GB) English, may be represented in preferred terms and other descriptions. They should be appropriately tagged using the Language Reference Set mechanism.

* For example,&#x20;
  * [191268006 | Chronic anemia (disorder)|](http://snomed.info/id/191268006)
    * FSN: Chronic anemia (disorder)
    * US PT: Chronic anemia
    * GB PT: Chronic anaemia
  * [414545008 | Ischemic heart disease (disorder)|](http://snomed.info/id/414545008)
    * FSN: Ischemic heart disease (disorder)
    * US PT: Ischemic heart disease
    * GB PT: Ischaemic heart disease

## Acronyms <a href="#acronyms" id="acronyms"></a>

Acronyms are easily misinterpreted. For this reason, acronyms are discouraged in FSNs.

* For example, the FSN should be the expanded form, Computed tomography of chest (procedure); however, as a preferred term, CT of chest (procedure) is acceptable.

If there is an unacceptable acronym in an existing FSN, the FSN DescriptionId is inactivated, and a new FSN is created (regardless of whether or not the acronym was in parentheses with the expanded form). The replacement FSN concept has the expanded description with the acronym entirely removed. Inactivating the ConceptId is not necessarily required, unless the FSN had significant ambiguity before changing it to its expanded form.  For more information on acronyms, see the [_Abbreviations and acronyms_](../#abbreviations-and-acronyms) section. &#x20;

## Imported FSNs <a href="#imported-fsns" id="imported-fsns"></a>

Before any changes are made to an FSN, imported directly with an extension (local) ID, the submitter should be notified and confirmation sought that no loss of meaning has occurred. This helps to ensure that the original meaning is understood and maintained. Authors should:

* Adhere to naming conventions.&#x20;
* Advise the submitter of changes and confirm that they are acceptable.
* Check for existing concepts with the same FSN; the term may be added as a preferred term or synonym.

{% hint style="warning" %}
**Original submitter**

Changes to existing SNOMED CT concepts do not necessitate notifying the original submitter.
{% endhint %}

## Semantic Tag <a href="#heading-title-text" id="heading-title-text"></a>

_Semantic tags_ are part of FSN descriptions. They are placed in parentheses at the end of FSNs when authoring concepts. They indicate the domain to which a concept belongs. For example: body structure, disorder, or specimen.

The purpose of semantic tags is to disambiguate concepts which have the same commonly used word or phrase.&#x20;

* For example,
  * Hematoma (morphologic abnormality)
  * Hematoma (disorder)

The following table contains the semantic tags for each domain.

| Domain                                                        | Semantic tags                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Body structure (body structure)                               | <ul><li><p>(body structure)</p><ul><li>(cell)</li><li>(cell structure)</li><li>(morphologic abnormality)</li></ul></li></ul>                                                                                                                                                                                                                                                      |
| Clinical finding (finding)                                    | <ul><li><p>(finding)</p><ul><li>(disorder)</li></ul></li></ul>                                                                                                                                                                                                                                                                                                                    |
| Environment or geographical location (environment / location) | <ul><li>(environment)</li><li>(geographic location)</li></ul>                                                                                                                                                                                                                                                                                                                     |
| Event (event)                                                 | <ul><li>(event)</li></ul>                                                                                                                                                                                                                                                                                                                                                         |
| Observable entity (observable entity)                         | <ul><li>(observable entity)</li></ul>                                                                                                                                                                                                                                                                                                                                             |
| Organism (organism)                                           | <ul><li>(organism)</li></ul>                                                                                                                                                                                                                                                                                                                                                      |
| Pharmaceutical / biologic product (product)                   | <ul><li>(clinical drug)</li><li>(medicinal product)</li><li>(medicinal product form)</li><li>(physical object)</li><li>(product)</li></ul>                                                                                                                                                                                                                                        |
| Physical force (physical force)                               | <ul><li>(physical force)</li></ul>                                                                                                                                                                                                                                                                                                                                                |
| Physical object (physical object)                             | <ul><li><p>(physical object)</p><ul><li>(product)</li></ul></li></ul>                                                                                                                                                                                                                                                                                                             |
| Procedure (procedure)                                         | <ul><li><p>(procedure)</p><ul><li>(regime/therapy)</li></ul></li></ul>                                                                                                                                                                                                                                                                                                            |
| Qualifier value (qualifier value)                             | <ul><li><p>(qualifier value)</p><ul><li>(administration method)</li><li>(basic dose form)</li><li>(calculation)</li><li>(disposition)</li><li>(dose form)</li><li>(intended site)</li><li>(product name)</li><li>(release characteristic)</li><li>(role)</li><li>(state of matter)</li><li>(transformation)</li><li>(supplier)</li><li>(unit of presentation)</li></ul></li></ul> |
| Record artifact (record artifact)                             | <ul><li>(record artifact)</li></ul>                                                                                                                                                                                                                                                                                                                                               |
| Situation with explicit context (situation)                   | <ul><li>(situation)</li></ul>                                                                                                                                                                                                                                                                                                                                                     |
| SNOMED CT Model Component (metadata)                          | <ul><li>(attribute)</li><li>(core metadata concept)<br><br></li><li>(foundation metadata concept)</li><li>(link assertion)<br><br></li><li>(linkage concept)<br><br></li><li>(namespace concept)<br><br></li><li>(OWL metadata concept)<br><br></li></ul>                                                                                                                         |
| Social context (social concept)                               | <ul><li><p>(social concept)</p><ul><li>(ethnic group)</li><li>(life style)</li><li>(occupation)</li><li>(person)<br><br></li><li>(racial group)</li><li>(religion/philosophy)</li></ul></li></ul>                                                                                                                                                                                 |
| Special concept (special concept)                             | <ul><li>(inactive concept)</li><li>(navigational concept)</li></ul>                                                                                                                                                                                                                                                                                                               |
| Specimen (specimen)                                           | <ul><li>(specimen)</li></ul>                                                                                                                                                                                                                                                                                                                                                      |
| Staging and scales (staging scales)                           | <ul><li><p>(staging scale)</p><ul><li>(assessment scale)</li><li>(tumor staging)</li></ul></li></ul>                                                                                                                                                                                                                                                                              |
| Substance (substance)                                         | <ul><li>(substance)</li></ul>                                                                                                                                                                                                                                                                                                                                                     |
