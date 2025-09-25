# Disorder Combination Modeling

Many disorders can occur in combination within the same patient. Guidance on the modeling and terming of FSNs for disorder combinations aims to achieve consistency. Clinically significant disorder combinations are represented in SNOMED CT by a single concept so that users can document temporal (timing) and causal (cause/effect) relationships between the conditions.

#### Expressing Associations <a href="#expressing-associations" id="expressing-associations"></a>

To express an association between conditions, one of the following associations is used:

* Simple co-occurrence: two or more conditions have no direct causal or temporal relationship but are found together more often than by random chance
* Causation 1: the cause is another finding or disorder, an event, or procedure
* Causation 2: the cause is a physical force, physical object, organism, or substance
* Temporal association: the timing of the two conditions occur before, during, or after each other

When considering disorder combinations two questions can be asked:

1. Is there a _causal_ relationship?
2. What is the _temporal_ relationship?

The following table provides the possible combinations of answers. It allows authors to assign combination disorders to a corresponding category below, to which the appropriate modeling and FSN construction is applied.

### Causal & Temporal Combinations

| Is there a stated causal relationship?                                           | Temporal relationship        | Resulting FSN pattern                |
| -------------------------------------------------------------------------------- | ---------------------------- | ------------------------------------ |
| **Yes – cause is another finding, disorder, event, or procedure (Causation 1)**  | Not stated                   | X due to Y                           |
|                                                                                  | After                        | X due to and following Y             |
|                                                                                  | Before                       | X before Y                           |
|                                                                                  | During                       | X due to and during Y                |
|                                                                                  | Before, During, and/or After | X due to and temporally related to Y |
| **Yes – cause is a physical object/force, organism, or substance (Causation 2)** | Not stated                   | X caused by Y                        |
|                                                                                  | After                        | N/A                                  |
|                                                                                  | Before                       | N/A                                  |
|                                                                                  | During                       | N/A                                  |
|                                                                                  | Before, During, and/or After | N/A                                  |
| **No stated causal relationship**                                                | Not stated                   | Document separately                  |
|                                                                                  | After                        | X after Y                            |
|                                                                                  | Before                       | X before Y                           |
|                                                                                  | During                       | X during Y                           |
|                                                                                  | Before / During / After      | X temporally related to Y\*          |

> _\*Note: |Temporally related to (attribute)| and its subtypes_ Before _and_ During _are only approved to model perioperative complications and a limited number of other clinical findings._

***

## **Simple Co-occurrence**

#### Naming pattern:

FSN: _X with Y_

#### Modeling pattern:

Assign each condition as a supertype (or ensure that each participating disorder is present in the ancestor tree following classification)

Use simple co-occurrence for two or more conditions that are strongly associated by means other than causality or a temporal relationship (e.g. a common predisposition) where representing such conditions as separate statements would result in a loss of the associated between the conditions

For example,

* Named syndromes, such as [398114001 | Ehlers-Danlos syndrome (disorder)|](http://snomed.info/id/398114001)
* Manifestations of systemic disorders, such as 83901003 |Sjögren's syndrome (disorder)|

Do not use simple co-occurrence for those disorders with more than one anatomical site or more than one associated morphology. Those disorders should rather be represented as individual concepts in a medical record.

### Example

#### C

####

{% hint style="warning" %}
Be aware of conditions which likely exist prior to a disorder or procedure.

For example, legacy term

[609454008 | Induced termination of pregnancy complicated by acute necrosis of liver (disorder)|](http://snomed.info/id/609454008)

*   _Acute necrosis of liver_ was likely present prior to the procedure; there is no explicit causation. The concept will be inactivated. Instead, separate concepts

    [714812005 | Induced termination of pregnancy (procedure)|](http://snomed.info/id/714812005)and[197269008 | Acute necrosis of liver (disorder)|](http://snomed.info/id/197269008) should be documented in the medical record.
{% endhint %}

***

{% hint style="success" %}
Be aware of conditions which likely exist prior to a disorder or procedure.

For example, legacy term

[609454008 | Induced termination of pregnancy complicated by acute necrosis of liver (disorder)|](http://snomed.info/id/609454008)

*   _Acute necrosis of liver_ was likely present prior to the procedure; there is no explicit causation. The concept will be inactivated. Instead, separate concepts

    [714812005 | Induced termination of pregnancy (procedure)|](http://snomed.info/id/714812005)and[197269008 | Acute necrosis of liver (disorder)|](http://snomed.info/id/197269008) should be documented in the medical record.
{% endhint %}

## **Causation 1**

Cause is another finding, disorder, event, or procedure

<table><thead><tr><th width="243.3125">Aspect</th><th>Guidance</th></tr></thead><tbody><tr><td>Modeling pattern</td><td>For disorders caused by another finding/disorder: use Due to relationship. Ensure appropriate supertypes and/or axioms. For procedures/events: represent caused condition as supertype and assign procedure/event as target of Due to.</td></tr><tr><td>Naming pattern</td><td><p>Use X due to Y.</p><p>For causal + temporal: use X due to and [temporal relation] Y.</p></td></tr><tr><td>Correct examples</td><td><p><em>Shock due to anaphylaxis (disorder)</em></p><p><em>Anemia due to blood loss (disorder)</em></p></td></tr><tr><td>Incorrect examples</td><td><p><em>Neutropenia associated with AIDS (disorder)</em> → should be <em>Neutropenia with AIDS (disorder)</em>.</p><p><em>Dilated cardiomyopathy secondary to granuloma (disorder)</em> → should be <em>…due to granuloma (disorder)</em>.</p></td></tr><tr><td>Notes</td><td>Avoid “co-occurrent and due to” phrasing; model as co-occurrence + Due to if clinically justified.</td></tr></tbody></table>

#### Correct examples:

* [735173007 | Shock due to anaphylaxis (disorder)|](http://snomed.info/id/735173007) is an example of a condition caused by a clinical finding/disorder. Because the shock and the anaphylaxis are co-occurring, both conditions are represented in the supertypes and axioms, in addition to the Due to relationship.
* [413532003 | Anemia due to blood loss (disorder)|](http://snomed.info/id/413532003) is an example of a condition caused by a clinical finding/disorder. Because the bleeding could have been controlled and thus not necessarily present, only causation is modeled in this concept. The blood loss/bleeding is not represented as a supertype.

#### Incorrect examples not to be repeated:

* Neutropenia associated with acquired immunodeficiency syndrome (disorder) - Do not use 'associated'; use only 'with' instead. So, |Neutropenia with acquired immunodeficiency syndrome (disorder)|.
* Dilated cardiomyopathy secondary to granuloma (disorder) - Do not use 'secondary to'; use 'due to' instead. So, |Dilated cardiomyopathy due to granuloma (disorder)|.

{% hint style="warning" %}
#### **Determining causation only versus causation and co-occurrence**

There are no heuristics to standardize the determination of a precoordinated combination modeled using only the _Due to_ relationship versus modeling the _Due to_ relationship in addition to representing the causative condition in the supertypes. If both conditions must be present for the other to occur, both should be represented in the supertypes. Whether both conditions must be present concurrently is determined by an understanding of the disease process. Considerations include whether the conditions are chronic diseases, as these types of conditions will be ever present and thus require representation in the supertypes. If the causing condition resolves but the resultant condition can remain, then representation of both conditions in the supertypes is unwarranted.

There are approximately 425 legacy concepts with '_co-occurrent and due_ _to'_ in the description. Do not add new concepts with the terming '_co-occurrent and due to'_, instead use co-occurrence modeling (both conditions are represented in a supertype) in addition to the _Due to_ (attribute) if warranted by the clinical condition.
{% endhint %}

## **Causation 2**

Causation 2 is when <sup>1</sup>the cause is a material entity, and <sup>2</sup>the means of exposure/introduction are not significant.

1. A material entity refers to a concept within the Substance, Physical object, Pharmaceutical/biologic product, Physical force, and Organism hierarchies.
2. If the means of exposure/introduction are significant, then the causal factor is represented by a concept from the Event hierarchy, and the concept is modeled as Causation 1.

### Summary

| Aspect             | Guidance                                                                                                                                                                                                                   |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition         | Cause is a material entity (substance, object, force, organism, pharmaceutical/biologic).                                                                                                                                  |
| Modeling pattern   | <p>Assign the caused disorder (X) as a supertype, or ensure that the caused disorder is a supertype following classification</p><p>Assign the causal factor (Y) as the value of a <em>Causative agent (attribute)</em></p> |
| Naming pattern     | X caused by Y                                                                                                                                                                                                              |
| Correct example    | _Contact dermatitis caused by chemical (disorder)_                                                                                                                                                                         |
| Incorrect examples | _Choking due to airway obstruction (finding)Coma associated with diabetes mellitus (disorder)Laser-induced burn (disorder)_                                                                                                |

### Correct example:

* [291000119100 | Contact dermatitis caused by chemical (disorder)|](http://snomed.info/id/291000119100)

### Incorrect examples not to be repeated:

* Choking due to airway obstruction (finding)
* Coma associated with diabetes mellitus (disorder)
* Laser-induced burn (disorder)

## **Temporal Sequencing (No Causation)**

Assign the condition or procedure that occurred first in the patient as the target of an After (attribute) relationship. Assign the condition that occurred second as a supertype (or ensure its presence in the ancestor tree).

Examples:

* 402490007 |Calcinosis following localized fat necrosis (disorder)|

The fat necrosis occurred first in the patient, so this concept will have an After (attribute) with a value of Fat necrosis (disorder). The calcinosis occurred secondarily, and thus Calcinosis (disorder) is a supertype of this concept.

* 16055031000119100 |Astigmatism of right eye following operative procedure (disorder)|

The operative procedure occurred first in the patient, so this concept will have an After (attribute) with a value of Surgical procedure (procedure). The astigmatism occurred secondarily, so Astigmatism (disorder) is a supertype of this concept.

### Summary

| Aspect           | Guidance                                                                                                                                                                          |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Modeling pattern | Assign first condition/procedure as target of After relationship. Assign second condition as supertype.                                                                           |
| Naming pattern   | <p>Where X occurs after Y:</p><ul><li>if it is not specified that X is due to Y (although causality is frequently implied), construct the FSN as <em>X following Y</em></li></ul> |
| Correct examples | _Calcinosis following localized fat necrosis (disorder)Astigmatism of right eye following operative procedure (disorder)_                                                         |

## Caution against combination <a href="#caution-against-combination" id="caution-against-combination"></a>

Not all disorders occurring in combination should be precoordinated into a single concept. Multiple clinical conditions should not be precoordinated in order to facilitate convenient recording in the medical record, even if the two conditions are often reported together.

* For example,
  * The clinical conditions _gastroenteritis_ and _dehydration_ often occur in combination but require separate resolution, and therefore, are best recorded separately in the medical record as 25374005 |Gastroenteritis (disorder)| and 34095006 |Dehydration (disorder)|.

## Associated with (attribute) <a href="#associated-with-attribute" id="associated-with-attribute"></a>

In general, [47429007 |Associated with (attribute)|](http://snomed.info/id/47429007) should be avoided due to the ambiguity which it conveys and the difficulty in applying this role consistently. Instead, _Due to_ is used when there is a direct causal relationship between the conditions; otherwise, the clinical conditions should be recorded as separate concepts in the medical record.

There are a couple of exceptions when the use of [47429007 |Associated with (attribute)|](http://snomed.info/id/47429007) is appropriate:

**General grouping concepts which aggregate more specific associations**

Example:

[6211002 |Polyarthritis associated with another disorder (disorder)|](http://snomed.info/id/6211002) subsumes two children:

* [201972000 |Allergic arthritis of multiple sites (disorder)|](http://snomed.info/id/201972000) modeled with [_42752001 |Due to (attribute)|_](http://snomed.info/id/42752001) of [419076005 |Allergic reaction (disorder)|](http://snomed.info/id/419076005)
* [422565003 |Post-infective polyarthritis (disorder)|](http://snomed.info/id/422565003) modeled with [_255234002 |After (attribute)|_](http://snomed.info/id/255234002) of [40733004 |Infectious disease (disorder)|](http://snomed.info/id/40733004)

#### Device infections

i.e an infection of the tissue surrounding an implanted or inserted device, not due to the device itself.\\

* _Associated with_ is used to associate the device with the infection.

#### Intolerance to substances

i.e the propensity of an adverse reaction to a substance to occur (other than hypersensitivity or allergic or non-allergic hypersensitivity).

#### There is no intolerance process that serves as the value for _Has realization_.

* _Associated with_ is used to associate the intolerance to the substance.

## When to use "caused by" and when to use "due to" <a href="#when-to-use-caused-by-and-when-to-use-due-to" id="when-to-use-caused-by-and-when-to-use-due-to"></a>

#### Is cause a disorder or material entity? <a href="#is-cause-a-disorder-or-material-entity" id="is-cause-a-disorder-or-material-entity"></a>

It must be determined if a disorder is caused either by another disorder or by a material entity. A material entity is a concept found in Substance, Physical object, Pharmaceutical/biologic product, Physical force, or Organism subhierarchies. These subhierarchies are the current range constraints for the Causative agent (attribute) in the Clinical finding domain. For combined disorders where a cause can be either a disorder (eg, alcoholism) or a material entity (eg, alcohol):

Model as _due to_ _disorder_ if it is the indirect cause.

* For example,
  * Megaloblastic anemia _due to_ _alcoholism_ (disorder)

Model as _caused by_ _material entity_ if it is the direct cause.

* For example,
  * Inflammation of pancreas _caused by alcohol_ (disorder)

#### Is cause a disorder or infectious organism? <a href="#is-cause-a-disorder-or-infectious-organism" id="is-cause-a-disorder-or-infectious-organism"></a>

In modeling concepts related to infectious diseases, a number of considerations need to be taken in to account.

1. When the disorder is an infectious disease itself, and the organism is specified, then the concept will be modeled with
   1. |Causative agent (attribute)| with the specified organism
   2. |Pathological process (attribute)| with the type of infectious process

2\. Disorders can be modeled with |Due to|, with |After|, or with both |Due to| and |After| relationships to infectious diseases.

* If the focus disorder is itself an infectious disorder, it will also have a |Causative agent| relationship when the organism is specified.

#### Examples

* **|Causative agent|** relationship
  * 721742004 |Otitis media caused by Streptococcus pneumoniae (disorder)|
* **|Due to|** relationship:
  * 698733009 |Intestinal obstruction due to tuberculosis (disorder)|
* **|Due to|** and **|Causative agent|** relationship:
  * 866044006 |Mycosis due to human immunodeficiency virus infection (disorder)|
* **|After|** relationship:
  * 182961000119101 |Acute disseminated encephalomyelitis following infectious disease (disorder)|
* **|After|** and **|Causative agent|** relationship:
  * 4740000 |Herpes zoster (disorder)|
* **|Due to|** and **|After|** relationship:
  * 1148594002 |Chronic arthritis due to and following rheumatic fever (disorder)|

{% hint style="warning" %}
_Applying the |Due to|, |After|, or both |Due to| and |After| relationships to a concept will not lead to it being a subtype of |Infectious disease (disorder)| unless it is itself an infectious disease._
{% endhint %}

Generally, when |Causative agent| is used in the concept's modeling, the terming 'caused by' is used in the FSN. Similarly, when |Due to| is used in the concept's modeling, the terming 'due to' is used in the FSN. In some situations, both the |Causative agent| and |Due to| are used in a concept's model, and so the naming may vary based on the situation.

In some cases, the DUE TO takes precedence because of a relationship between the causative agent and the DUE TO disorder.

**For example,**

288021000119107 |Disorder due to alcohol abuse (disorder)|

<figure><img src="../../../../../.gitbook/assets/image (8) (1) (1) (1).png" alt=""><figcaption><p>Stated form of |Disorder due to alcohol abuse (disorder)|</p></figcaption></figure>

In other cases, the DUE TO relationship is used as a means to classify the concept appropriately while the CAUSATIVE AGENT takes precedence.

**For example,**

1251395000 |Injury of skin caused by class Anthozoa (disorder)|

<figure><img src="../../../../../.gitbook/assets/image (9) (1) (1) (1).png" alt=""><figcaption><p>Inferred form of |Injury of skin caused by class Anthozoa (disorder)|</p></figcaption></figure>

In this case, the DUE TO represents the "injury" part of the concept and allows classification as a traumatic injury. An alternative, but less appealing FSN would have been "Disorder of skin due to traumatic injury caused by class Anthoza". So, if the concept FSN specifies a disorder causally associated with another disorder, then use "due to" in the FSN; if the FSN specifies a disorder causally associated with an "agent" (organism, physical object, substance, etc.), then use "caused by" in the FSN.

## Exception to naming convention for combined disorders <a href="#exception-to-naming-convention-for-combined-disorders" id="exception-to-naming-convention-for-combined-disorders"></a>

Exceptions may exist to the above guidance which requires review on a case-by-case basis.

The FSN submitted by a requestor may be used as preferred term even if it does not comply with the above recommended pattern. However, do not use phrases such as _secondary to_, _as a result of_, etc., in lieu of _due to_.

Rather than the naming conventions described above, use the names that are accepted clinical parlance and that represent specific pathophysiologic entities for some combined disorders, as the preferred term.

The stricter rules for FSN construction do not prevent the addition of more familiar connectives in other descriptions, for example _with,_ or _associated with_.

**Disorder combination modeling**

* Covers combinations of only two disorders. However, combinations often include more than two disorders (for example, syndromes). Document multiple conditions in a single statement only for syndromes or strong associations based on a common predisposing factor.
* Does not cover absent components or _negation_
* Does not cover cases where combination concepts are demonstrably classification-derived (This limitation accepts that some content may be so obviously based on a class or category in a classification that it would be undesirable to reinterpret its semantics.)
* The modeling approach may be difficult to apply in all cases of combined disorders; domain-specific templates should be developed to ensure modeling consistency and accuracy.
