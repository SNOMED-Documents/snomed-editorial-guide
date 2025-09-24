# Laterality

## Determine if an anatomy structure is lateralizable

The anatomy structures should only be pre-coordinated with laterality if they are lateralizable. All anatomy structures on the midline are not lateralizable. The Lateralizable Body Structure Reference Set has been developed and published as part of SNOMED International release. Please note that the refset requires an ongoing update for new additions.

{% hint style="info" %}
In this guide, the lateralizable anatomy structures are divided into three types:

* **X**
  * The type X represents any anatomy structure that is lateral to mid-sagittal plane.
* **Lateral half of Y**
  * Y represents any anatomy structure that is symmetrical on the body's middle-line which cannot be lateralized. However, the lateral half of Y can have laterality, e.g. right half of head.
* **{Part} of X or Y**
  * {Part} represents any constitutional or regional part of anatomical structure of X or lateral half of Y.
{% endhint %}

## Creation of lateralized anatomy structure

Both Left and Right structures must be added when adding the new pre-coordinated concepts for anatomy structure with laterality. Lateralization should not be routinely applied to Entire and Part of anatomy concepts unless the concept model requires such lateralized anatomy structure.

_Bilateral X anatomical structure (body structure)_ must not be added. The concepts under `422525002 |Structure of bilateral paired structures (body structure)|` are no longer in use in the international edition of SNOMED CT because bilateral concepts are defined by two role groups. However, these concepts may still be in use by extensions, in post-coordinations, or as values in information models. We would recommend users to review their usage and provide feedback to us. Users will be consulted before these concepts are ultimately inactivated.

## Term patterns for laterality

Following are the most common term patterns for the representation of laterality for anatomy structures. Preferred terms should have the same description without a semantic tag. In descriptions in hierarchies such as clinical finding/disorder, procedure, observable entity, and situation with explicit context, 'structure of' can be omitted when body site is not a concept of Entire anatomy entity.

### Structure of + left/right + X or Structure of + left/right + half of Y

* Structure of left hand (body structure)
* Structure of right lung (body structure)
* Structure of left ring finger (body structure)
* Structure of left renal artery (body structure)
* Bone structure of left tibia (body structure)
* Structure of right half of head (body structure)
* Structure of right cerebral hemisphere (body structure)

### Structure of + {part} + left/right + X or Structure of + {part} + left/right + half of Y

* Bone structure of left hand (body structure) - bone structure is constitutional part of hand
* Bone structure of phalanx of left ring finger (body structure)
* Skin structure of right foot (body structure) - skin structure is constitutional part of foot
* Skin structure of left index finger (body structure)
* Bone structure of proximal right humerus (body structure) - proximal is regional part of humerus
* Bone structure of shaft of left femur (body structure) - shaft is regional part of femur

### **Special cases that are different from the above two common term patterns**

#### Finger/toe

Finger/toe is not sufficient - Laterality should be placed before hand/foot when finger/toe or any part of a finger/toe is not further specified to individual digit, e.g., ring finger, index finger, great toe.

| Example                                                                 | Evalution                                                                                                                                                                                                                                                                                                                |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Structure of finger of left hand (body structure)                       | :green\_circle: correct                                                                                                                                                                                                                                                                                                  |
| Structure of left finger (body structure)                               | :red\_circle: incorrect                                                                                                                                                                                                                                                                                                  |
| Bone structure of phalanx of finger of left hand (body structure)       | :green\_circle: correct                                                                                                                                                                                                                                                                                                  |
| Bone structure of phalanx of left finger (body structure)               | :red\_circle: incorrect                                                                                                                                                                                                                                                                                                  |
| Structure of nail of toe of right foot (body structure)                 | <p><span data-gb-custom-inline data-tag="emoji" data-code="1f534">🔴</span> incorrect , neither 'right nail' nor 'right toe' is correct</p><p><strong>Note</strong>, hand/foot is redundant when an individually named finger, e.g. index finger, or the great toe has been specified in a description. For example,</p> |
| Bone structure of phalanx of left index finger (body structure)         | :green\_circle:correct                                                                                                                                                                                                                                                                                                   |
| Bone structure of phalanx of index finger of left hand (body structure) | :orange\_circle: it is not wrong, but 'hand' is redundant                                                                                                                                                                                                                                                                |
| Bone structure of phalanx of left index finger of hand (body structure) | :orange\_circle: it is not wrong, but 'hand' is redundant                                                                                                                                                                                                                                                                |

#### Structure of + {non lateralizable part} + left/right lung

Parts of symmetric structures should be symmetric. However, some body parts are exceptions. The laterality value in modeling is inherited from its lateralizable parent concept, e.g. left/right lung structure. Therefore, descriptions must clearly indicate such inheritances to avoid potential confusion. It is not accurate for a term such as "right middle lobe" because there is no "left middle lobe". The following are examples for correct description pattern. Note: existing content has not been following the term pattern.

#### Structure of + {part} + left/right half of Y

Leave the new concept as primitive if concept 'Structure of half of Y lateral to mid-sagittal plane (body structure)' does not exist. The new concept for 'Structure of half of Y lateral to midsagittal plane' should not be added until the policy is developed.

{% hint style="info" %}
See also the policy for a preferred term in relationship to Structure vs. Entire at [Naming Convention for SEP Model](../index/naming-convention-for-sep-model.md).
{% endhint %}

## Concept modeling for laterality

The 'part of' relationship should not be used for concept modeling in anatomy. The laterality attribute should be the only attribute for the representation of laterality. The new concept model for anatomy has not been implemented, and the proximal primitive modeling style should not be applied.

For term pattern 1, the concept X or lateral half of Y should be used to fully define a concept with laterality, as shown in these examples:

<figure><img src="../../../../../.gitbook/assets/image (13) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/domain-specific-modeling/body-structure/anatomical-concept-model/images/174690328.png" alt=""><figcaption></figcaption></figure>

For term pattern 2, the pre-coordinated concept {part} of X should be used to fully define the concept with laterality. Note: Concepts for which an identifier has not been assigned have been shown with an identifier of '1111111111'.

For example,

<figure><img src="../../../../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

Please note that the concept modeling and utility of pre-coordinated concepts of 'structure of {part} of lateral half of Y' and 'structure of half of Y lateral to mid-sagittal plane' are still under investigation. Similar new anatomy concepts should not be added. The concept model should only use existing pre-coordinated concept {part} of lateral half of Y.

For example,

<figure><img src="../../../../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

If pre-coordinated concept does not exist for '{part} of structure of half of Y' or 'structure of half of Y lateral to mid-sagittal plane', the concept can be defined by {part} of Y and the definition status should be primitive.

For example, concept |Structure of lateral half of lower back| does not exist, the concept 'Structure of left half of lower back' should be defined as a primitive concept. Two parent concepts are expected: `61379005 |Structure of left side of trunk (body structure)|` and `37822005 |Lower back structure (body structure)|`. The additional parent |Structure of left side of trunk (body structure)| is to ensure that any lateralized concept must be a subconcept of a lateralizable structure.

<figure><img src="../../../../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/domain-specific-modeling/body-structure/anatomical-concept-model/images/174690331.png" alt=""><figcaption></figcaption></figure>
