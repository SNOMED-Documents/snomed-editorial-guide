# Changes to Components

## Considerations for current concepts when creating new concepts

Concepts that are used as target values in an attribute relationship impact the placement of the source concept of the relationship. Some concepts, for example, those in the Qualifier value hierarchy, are created to support the definition of other concepts. Creation of a new concept that will be used as the target value in an attribute relationship requires an author to determine if there are active concepts in the _domain_ hierarchy that should also use the new concept as a target value.

For example,

The creation of [713295009 | Surgical replacement - action (qualifier value)|](http://snomed.info/id/713295009) would require a review of active concepts that represent _surgical_ replacement procedures that were previously modeled with the Method (attribute) of Replacement - action (qualifier value).

A concept that represents a surgical replacement procedure that currently has a Method (attribute) of [282089006 | Replacement - action (qualifier value)|](http://snomed.info/id/282089006) would require inactivation of that relationship and the creation of a new attribute-value relationship of Method (attribute) of [713295009 | Surgical replacement - action (qualifier value)|](http://snomed.info/id/713295009).

## Description Inactivation

**Description inactivation values**

Depending upon the combination of the type of component and the reason for inactivation, a specific inactivation reason must be selected.

| Inactivation value                                                         | Definition                                                                                                                                                                                                                                                                                                     | Example                                                                                                                                                                              |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Not semantically equivalent component (foundation metadata concept)        | A description does not represent the same meaning as the concept's Fully Specified Name (FSN)                                                                                                                                                                                                                  | Removal of device (procedure) has a synonym, Replacement of prosthetic device (procedure), which should be inactivated because the synonym has a more specific meaning than the FSN. |
| Outdated component (foundation metadata concept)                           | A component is no longer current, useful, appropriate or acceptable                                                                                                                                                                                                                                            | The synonym _Compression facies_ was inactivated from the concept's more modern description of _Facial asymmetry_.                                                                   |
| Grammatical description error (foundation metadata concept)                | <p>A component contains a technical error.</p><p>The error in the description is grammatical or a spelling mistake, which when corrected does not change the meaning of the concept. Where the meaning <em>is</em> changed, the <em>concept</em> should be inactivated using <em>Erroneous component</em>.</p> | <p>Case significance error: <em>Alpha</em> should have a lower case <em>a</em></p><p>Spelling error: <em>Asthma</em> misspelled as <em>Assthma</em></p>                              |
| Nonconformance to editorial policy component (foundation metadata concept) | A component fails to comply with the current editorial guidance                                                                                                                                                                                                                                                | <p>The concept Urine: turbid (finding) was inactivated and replaced by</p><p><a href="http://snomed.info/id/167238004">167238004</a></p>                                             |

### Order of selection of inactivation values <a href="#order-of-selection-of-inactivation-values" id="order-of-selection-of-inactivation-values"></a>

When there is more than one reason to inactivate a description, the order of preference for the inactivation value is as follows:

1. [723278000 | Not semantically equivalent component (foundation metadata concept)|](http://snomed.info/id/723278000)
2. [900000000000483008 | Outdated component (foundation metadata concept)|](http://snomed.info/id/900000000000483008)
3. [1217318005 | Grammatical description error (foundation metadata concept)|](http://snomed.info/id/1217318005)
4. [723277005 | Nonconformance to editorial policy component (foundation metadata concept)|](http://snomed.info/id/723277005)

### Corresponding association type <a href="#corresponding-association-type" id="corresponding-association-type"></a>

Only the description inactivation value of _Not semantically equivalent_ _component_ requires an association type; the association type is _Refers to_ and necessitates the reference to at least one active SNOMED CT concept. It is possible that the description is ambiguous and may relate to more than one concept.

The other three description inactivation values (outdated, grammatical error, nonconformance) do not require an associated concept.

{% hint style="info" %}
See also, _Changes in FSN_, on the [Fully Specified Name](https://conf.spaces.snomed.org/wiki/spaces/DOCEG/pages/133244331) page.
{% endhint %}

## Concept Inactivation

### Concept inactivation values <a href="#concept-inactivation-values" id="concept-inactivation-values"></a>

A value from the choices below must be chosen as a reason for inactivating a concept. Inactivation replacement associations are ultimately at the author's discretion. Especially in the instance of an infinite number of possible replacements, clinical relevance and subset inclusion should be considered. Non-synonymous synonyms should also be inactivated and reassigned.

### Inactivation Associations

| Inactivation reason                     | Association type                   | Cardinality | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| --------------------------------------- | ---------------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Ambiguous**                           | Possibly equivalent to             | 1..\*       | <p>• The inactivated concept is inherently ambiguous.<br>• Every effort should be made to identify all clinically useful POSSIBLY_EQUIVALENT_TO target concepts, as close as possible to the meaning of the inactivated concept.<br>• New concepts should be created if clinically valid.<br>• Target may be singular where the second target has little or no clinical usefulness.<br>• It is not necessary to represent all semantic meaning if concepts should not exist in SNOMED CT.<br>• If the FSN is vague (not ambiguous), consider using <em>Meaning of component unknown</em>.</p> |
| **Classification-derived component**    | Replaced by                        | 0..1        | <p>• Applies to concepts with classification-type descriptions, which do not have to appear in a classification.<br>• Use with “not otherwise specified” (NOS), “not elsewhere classified” (NEC), “unspecified”, “other”.</p>                                                                                                                                                                                                                                                                                                                                                                 |
|                                         | Partially equivalent to            | 0..\*       | <p>• Use when the intended meaning is a disjunction for classification purposes (“with”, “and”, “and/or”).<br>• Replacements must include all clinically valid elements of the disjunction.<br>• Every effort should be made to identify all clinically valid targets.<br>• New concepts should be created where appropriate.</p>                                                                                                                                                                                                                                                             |
| **Duplicate component**                 | Same as                            | 1..1        | • The concept is inactive because it has the same meaning as another concept.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Erroneous component**                 | Replaced by                        | 1..1        | <p>• Applies to FSNs with an error that, when corrected, potentially changes the semantic meaning.<br>• If the error is grammatical or spelling only, and correction does not change meaning, the description (not concept) should be inactivated.</p>                                                                                                                                                                                                                                                                                                                                        |
| **Meaning of component unknown**        | No association type applied        | 0..0        | <p>• The meaning of the concept cannot be determined.<br>• The FSN is vague, not ambiguous.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Non-conformance to editorial policy** | No suitable replacement identified | 0..0        | <p>• A suitable replacement cannot be identified, or the concept is out of scope (e.g., administrative, occupation, country).<br>• No replacement is required when jurisdictional control passes between extensions.<br>• Applies to concepts not adhering to editorial guidelines (e.g., groupers that cannot be defined, or naming pattern violations).</p>                                                                                                                                                                                                                                 |
|                                         | Replaced by                        | 0..1        | • Used where editorial conformance potentially changes meaning, and a semantically close replacement exists.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|                                         | Alternative                        | 0..\*       | • Used when editorial policy changes scope (e.g., branded products are out of scope — alternative is the generic product).                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Outdated component**                  | No suitable replacement identified | 0..0        | <p>• Concept is outdated and no longer clinically acceptable or interoperable internationally.<br>• May simply fall into disuse without replacement.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|                                         | Possibly replaced by               | 0..\*       | • Used when two or more potential replacements exist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|                                         | Replaced by                        | 0..1        | • Used when a semantically similar or more general replacement exists, mainly for reconciling historical data.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

{% hint style="info" %}
**Historical relationships**

When changes are made to a historical relationship for a concept that was previously inactivated, such as Limited/WAS\_A, assign a new historical relationship that facilitates traceability of the concept (duplicate, ambiguous, classification derived, etc.). The _Limited component_ inactivation reason (WAS\_A association type) is no longer in use for new content inactivations as of the July 2018 release.
{% endhint %}

### Inactivation Reasons <a href="#ambiguous" id="ambiguous"></a>

#### Ambiguous <a href="#ambiguous" id="ambiguous"></a>

All possible meanings should be represented in the replacement targets when feasible, creating new concepts as replacements when appropriate.

Ambiguous concepts with a single replacement target may be used if one of the two possible meanings of the ambiguous concept is not clinically useful.

#### Classification-derived <a href="#classification-derived" id="classification-derived"></a>

Many, but not all, concepts precoordinated with "with" and "and" are derived from classifications; regardless, this is the acceptable inactivation reason.

For concepts with exclusions, such as NEC, NOS, etc., use the _Replaced by_ association with the immediate parent concept as the value, which is the clinical condition without any context. If a parent concept without the exclusion does not exist, it should be created as a new concept.

For concepts with conjunctions such as 'and' and 'with', use the _Partially equivalent to_ association with the two separate values as targets. For the purposes of patient care, it is recommended that each disorder is recorded individually.

The _Partially equivalent to_ association signifies that **all** applied targets must be implemented within the clinical notes to ensure the original clinical idea is represented.

#### Duplicate <a href="#duplicate" id="duplicate"></a>

#### _Inactivation_ <a href="#inactivation" id="inactivation"></a>

* Note that the meaning of the concept is based on the FSN but does not imply that the FSNs are identical.\
  Keep the concept with the more specific FSN. FSN is the source of a concept's meaning; hence, there should be more weight in the meaning of the FSN rather than the underlying modeling. Implementers do not see modeling.
* If appropriate, add the descriptions from the inactivated concept to the remaining active concept while ensuring they are semantically equivalent, clinically useful, and follow current naming conventions.

#### _Consider_ <a href="#consider" id="consider"></a>

* Inactivating the newer concept
* Inactivating the concept with fewer subtypes. This will simplify the process and minimize the amount of rework required.
* Inactivating the concept with least modeling
* Updating the retained concept's FSN and modeling to align with current policy.

#### _Differing hierarchies_ <a href="#differing-hierarchies" id="differing-hierarchies"></a>

The Duplicate component is the inactivation for duplicated concepts:

1. Within the following hierarchies:
   1. Clinical finding and Disorder
   2. Procedure and Regime/Therapy
2. Between the following top-level hierarchies:
   1. Clinical finding and Situation
   2. Procedure and Situation
   3. Observable and Procedure

Any possible duplicates between concepts among other paired hierarchies not listed above should be reconsidered as duplicates and directed to another inactivation reason, likely Erroneous.

{% hint style="warning" %}
If the change is a request, inform the requestor as to which concept is inactivated.
{% endhint %}

#### Erroneous <a href="#erroneous" id="erroneous"></a>

Where the error gives rise to potential ambiguity, use the inactivation reason of Ambiguous component. Otherwise, the Erroneous component requires a single _Replaced by_ value.

#### Meaning unknown <a href="#meaning-unknown" id="meaning-unknown"></a>

Meaning of the concept is unknown, and an association type is not given. It will normally be necessary to search the clinical literature to establish that this is truly an unknown concept rather than an outdated clinical concept.\
This inactivation reason may be used where the meaning of the FSN is considered to be vague.

#### Nonconformance to editorial policy <a href="#nonconformance-to-editorial-policy" id="nonconformance-to-editorial-policy"></a>

Concept which do not adhere to editorial guidance can be inactivated without an association type. Else _Replaced by_ and _Alternative_ are Association type options.

Policies will often delineate how these two _Association type_ options will be used. Changes of this type often include bulk updates and may relate to medicinal products, substances, and devices.

#### Outdated <a href="#outdated" id="outdated"></a>

When an outdated concept simply falls into disuse without any appropriate replacement, no historical association is applied.

_Replaced by_ is used for a single replacement concept that is semantically similar to or more general than the inactivated concept.

Possibly replaced by is used for multiple replacement concepts.

For example,

A substance or organism originally believed to be a single entity has been reclassified as two or more substances or organisms.

{% hint style="info" %}
**Reactivation**

[Management of Inactivated International Concepts within an Extension](https://app.gitbook.com/s/3RKZIWpWFT0ocCgNT16E/5-key-steps/5.4-authoring/5.4.1-general-authoring-principles/5.4.1.3-management-of-inactivated-international-concepts-within-an-extension "mention")
{% endhint %}
