# Lateralized Disorder Naming Conventions

{% hint style="warning" %}
**For more information**

See also Anatomical Structure Naming Conventions section [Naming Convention for Digits of Hand and Foot](../../body-structure/index/naming-convention-for-digits-of-hand-and-foot.md) and Laterality section [Laterality](../../body-structure/anatomical-concept-model/laterality.md)
{% endhint %}

## Right, left disorder concepts

When creating a lateralized disorder concept, two concepts should be created:

1. concept for the left side
2. concept for the right side

Descriptions

* FSN: \<morphologic abnormality> of \_right/left\_ \<body structure> (disorder)
* PT: _Right/left_
  * For example, 1089071000119109 | Inflammation of left mastoid (disorder)|
    * FSN: Inflammation of left mastoid (disorder)
    * PT: Left mastoiditis

<figure><img src="../../../../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption><p>Stated view of Inflammation of left mastoid (disorder)</p></figcaption></figure>

When creating a lateralized disorder concept, if a non-lateralized parent does not exist, then it should be created as well. In other words, do not just create the right and left versions, but also create a concept to represent the laterality-agnostic parent.

* For example,
  * When creating _Inflammation of left mastoid_ and _Inflammation of right mastoid_, also ensure a concept for _Inflammation of mastoid_ exists.

Where the disorder is left/right of a specific anatomical site, and the preferred term naming pattern of _Right/left_ causes a combination that does not sound like natural flowing English, the guidance above can be circumvented. See the section [Naming Convention for Digits of Hand and Foot](../../body-structure/index/naming-convention-for-digits-of-hand-and-foot.md) and Laterality section [Laterality](../../body-structure/anatomical-concept-model/laterality.md).

* For example,
  * _Left interphalangeal thumb joint open traumatic dislocation_ should follow naming guidance of _Open traumatic dislocation of interphalangeal joint of left thumb_.
  * _Left abscess of foot_ is an incorrect term; instead, this should read _Abscess of left foot_. &#x20;

{% hint style="info" %}
**Unilateral**

With the addition of lateralized content in the International Release, the need for unspecified unilateral concepts is removed, as well as potentially dangerous, if used directly in a patient record. Unilateral concepts are not accepted.
{% endhint %}

## Bilateral disorder concepts

Where the bilateral disorder description causes a combination that does not sound like natural flowing English, the guidance below can be circumvented.

#### When the body structure and the morphologic abnormality are combined into one word, the following naming pattern applies:

* FSN: of bilateral (disorder)
* PT: Bilateral
* SYN: of bilateral
* SYN: of both
* For example, 1084011000119100 | Inflammation of bilateral mastoids (disorder)|
  * FSN: Inflammation of bilateral mastoids (disorder)
  * PT:  Bilateral mastoiditis
  * SYN:  Inflammation of bilateral mastoids
  * SYN:  Inflammation of both mastoids

### When the body structure and morphologic abnormality are separate, the following naming pattern applies:

* FSN: of bilateral (disorder)
* PT: of bilateral
* SYN: of both

Note the PT of Bilateral is not required. _Bilateral_ is to describe the body site, not the morphologic abnormality.

*   For example,&#x20;

    15725081000119100 | Effusion of joint of bilateral feet (disorder) |

    * FSN:  Effusion of joint of bilateral feet (disorder)
    * PT:  Effusion of joint of bilateral feet
    * SYN: Effusion of joint of both feet

Also note that _joint_ is singular. This is to denote that the joint may be singular on each side of the body; the plurality of feet will represent the laterality. Using _joints_ as plural may incorrectly reflect that there are multiple joints affected in both feet.

{% hint style="warning" %}
Do not use _both_ to describe disorders of the eyelids unless the concept's means _both upper eyelids_ or _both lower eyelids_ , only then can that synonym be included for bilateral eyelid disorder concepts.
{% endhint %}

## Modeling of bilateral disorders

Bilateral disorders should be modeled using two relationship groups, one for each lateralized body structure.

<figure><img src="../../../../../.gitbook/assets/image (7) (1) (1) (1) (1).png" alt=""><figcaption><p>Stated view of Inflammation of bilateral mastoids (disorder) with a role group for each side</p></figcaption></figure>

{% hint style="info" %}
**Structure, Structure of**

Lateralized disorder concepts should not include the words _structure_ or _structure of_.

* For example,&#x20;
  * With use of 266005 | Structure of lower lobe of right lung (body structure)|,
    * a disorder concept is termed 724056005 | Malignant neoplasm of lower lobe of right lung (disorder)|
    * a procedure is termed 726425007 | Lobectomy of lower lobe of right lung (procedure)|
{% endhint %}






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=SCT+Editorial+Guide&entry.670899847=Lateralized%20Disorder%20Naming%20Conventions" class="button primary">Provide Feedback</a>
