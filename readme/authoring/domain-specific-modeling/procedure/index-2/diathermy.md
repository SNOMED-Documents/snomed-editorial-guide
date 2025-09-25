# Diathermy

The term _Diathermy_ has been used to refer to a broad array of procedures aimed at performing different types of actions and outcomes.  In SNOMED CT, the term diathermy may refer to 3 different kinds of procedures:

#### **Therapeutic diathermy:**

#### _1. A treatment that provides deep heat to the tissues without destructive action._

* Therapeutic application of conductive heat using heated pads, water, or other materials to promote healing.
* Employment of physical agents that convert high-frequency electric current or electromagnetic waves to deep heat to promote healing.&#x20;

#### **Surgical diathermy:**

_**2. The use of energy to destroy tissue for different purposes.**_&#x20;

* A procedure in which tissue is heated to destroy abnormal cells. The heat may be using different types of energy.&#x20;

_**3. The use of heat as a destructive procedure to perform a "secondary" action. e.g. Reattachment, repair.**_

Careful review of the intention of a procedure stating the term _diathermy_ in the descriptions should be done. The term _diathermy_ may be used to name non-destructive procedures. Before naming and modeling such concepts, be sure to carefully read this guide and the associated templates.

## 274071003 |Surgical diathermy (procedure)| <a href="#id-274071003-or-surgical-diathermy-procedure-or" id="id-274071003-or-surgical-diathermy-procedure-or"></a>

### Definition  <a href="#definition" id="definition"></a>

Destructive procedure performed by applying electrical energy to heat biological tissues.  The term _Surgical Diathermy_ refers to different types of surgical actions performed using electricity (e.g., electrocauterization, electrocoagulation, electrodesiccation). To consistently name the different types of actions and to accurately differentiate them, the descriptions must be based on the specific action stated in the description and secondarily on the term _diathermy_.&#x20;

### **Naming**

When a specific destructive action (cauterization, coagulation, desiccation) is stated in descriptions, use that action in the FSN for the concept and avoid the inclusion of the term _Diathermy_. Additionally, add "using electrical energy" to the FSN.  The use of the prefix "electro-" to describe a destructive action using electricity is no longer required in the FSN but will be retained on concepts as Preferred or Acceptable description in concepts where such a description was previously used, for searchability and retrieval.

**FSN: \[Action] of \[morphologic abnormality] of \[body structure] using electrical energy (procedure)**

* For example,
  * 232597008 |Bronchoscopic **cauterization** of lesion **using electrical energy** (procedure)|

**PT: \[Action] of \[morphologic abnormality] of \[body structure] using electrical energy**

* For example,
  * **Cauterization** of lesion of vagina **using electrical energy** (procedure)

**SYN: Electro-\[Action] of \[morphologic abnormality] of \[body structure]**

* For example,
  * Electrocauterisation of urinary bladder

If a specific non-destructive action (e.g., repair, reattachment) is included in the FSN along with the term diathermy, the descriptions should follow the pattern below:

**FSN: \[Action] of \[morphologic abnormality] of \[body structure] by diathermy (procedure)**

* For example,
  * 57103007 |**Reattachment** of retina **by diathermy** (procedure)|

**PT: \[Action] of \[morphologic abnormality] of \[body structure] by diathermy**

* For example,
  * **Repair** of retinal tear or defect **by diathermy**

When the FSN states the phrase, “Diathermy of X”, without any other considerations, a destructive action using Electrical energy should be inferred.  In these cases, using the term _Diathermy_ is allowed in the FSN and PT given that the specific action (e.g. coagulation, cauterization, etc.) is not stated.  The destructive action (named Surgical diathermy) may be applied to a Morphologic abnormality or to a Body structure.

Before modeling this type of concept, make sure that the concept is not referring to Therapeutic diathermy (regime/therapy) (e.g. Microwave therapy), if the concept is not a destructive but therapeutic diathermy procedure, please refer to Therapeutic diathermy below.

**FSN: Diathermy of \[morphologic abnormality] of \[body structure] (procedure)**

* For example,
  * 301876002 |**Diathermy** of **wart** (procedure)|

**PT: Diathermy of \[morphologic abnormality] of \[body structure]**

* For example,
  * **Diathermy** of **fallopian tube**

{% hint style="success" %}
**See templates:**&#x20;

[\[Action\] of X by diathermy (procedure) / \[Action\] of X using electrical energy (procedure)](https://conf.spaces.snomed.org/wiki/spaces/SCTEMPLATES/pages/134001529)

[Diathermy of X (procedure)](https://conf.spaces.snomed.org/wiki/spaces/SCTEMPLATES/pages/134001537)
{% endhint %}

## 1287433006 |Therapeutic diathermy (regime/therapy)| <a href="#id-1287433006-or-therapeutic-diathermy-regime-therapy-or" id="id-1287433006-or-therapeutic-diathermy-regime-therapy-or"></a>

### Definition  <a href="#definition.1" id="definition.1"></a>

Diathermy used for non-surgical/non-destructive procedures, e.g. physical therapy and chiropractics.  To avoid confusion between surgical and non-surgical diathermy procedures, Therapeutic diathermy procedures should be described including the energy used in the procedure, and must be stated on the FSN. These procedures are subsumed by 91251008 |Physical therapy procedure (regime/therapy)|.

### **Naming**

Use the name of the energy used in the procedure (e.g., microwave, conductive heat, shortwave) followed by the term _diathermy_, then "to", and finally the "Anatomical or acquired body structure" where the procedure is applied.

**FSN: \[Physical force] diathermy to \[body structure] (regime/therapy)**

**PT: \[Physical force] diathermy to \[body structure]**

* For example,
  * 306876003 |**Microwave** diathermy to lower limb (regime/therapy)|
  * 304394001 |**Short wave** diathermy to neck (regime/therapy)|
  * 49913004 |**Ultrashort wave** diathermy (regime/therapy)|

{% hint style="success" %}
**See template:**

[Therapeutic diathermy (regime/therapy)](https://conf.spaces.snomed.org/wiki/spaces/SCTEMPLATES/pages/134001523)
{% endhint %}

### Exclusions <a href="#exclusions" id="exclusions"></a>

When the specific surgical action ("by coagulation", "by cauterization") is stated, but there is neither any mention of the type of physical force used nor the term diathermy stated in the descriptions, the concept should not be considered a diathermy procedure. Do not use any prefix or the term _diathermy_ in descriptions.

These types of procedures should be classified in other hierarchies, e.g. Cauterization procedure (procedure), Coagulation procedure (coagulation).&#x20;

**FSN: \[Action] of \[morphologic abnormality] of \[body structure] (procedure)**

**PT: \[Action] of \[morphologic abnormality] of \[body structure] (procedure)**

**FSN: \[Action] of \[morphologic abnormality] of \[body structure] by \[Action] (procedure)**

**PT: \[Action] of \[morphologic abnormality] of \[body structure] by \[Action] (procedure)**



* For example,
  * 56121000 |**Repair** of arteriovenous fistula by **coagulation** (procedure)|
  * 1287542001 |**Coagulation** of external ear (procedure)|
  * 15593007 |**Cauterization** of pharynx (procedure)|






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=SCT+Editorial+Guide&entry.670899847=Diathermy" class="button primary">Provide Feedback</a>
