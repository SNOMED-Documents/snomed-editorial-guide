# Procedure Attributes

The following defining attributes correspond to the [_Procedure Attributes Summary_](../) table.

{% hint style="info" %}
**Self-grouped Attributes**

The following attributes are self-grouped, meaning they are not grouped with any other attributes:

* Priority
* Has focus
{% endhint %}

## Access

Access (attribute) describes the route used to access the site of a procedure. It distinguishes open, closed, and percutaneous procedures.

For example,

* 174572001 | Open removal of bile duct stent (procedure)| has Access of Open approach - access (qualifier value)

## Direct device

Direct device (attribute) represents the device on which the method directly acts.

For example,

* 431698006 | Adjustment of gastric banding using fluoroscopic guidance (procedure)| has Direct device of Surgical band (physical object)

{% hint style="success" %}
_Subtypes of Surgical repair (procedure) that include a prosthetic device should be modeled using the DIRECT DEVICE attribute when the value is <<53350007 |Prosthesis, device (physical object)|_
{% endhint %}

## Direct morphology

Direct morphology (attribute) describes the morphologically abnormal structure that is the direct object of the Method action.

For example,

* 31512000 | Shaving of benign lesion with chemical cauterization (procedure)| has the Direct morphology of Lesion (morphologic abnormality)

## Direct substance

Direct substance (attribute) describes the Substance or Pharmaceutical/biologic product on which the procedure's method directly acts.

For example,

* 231274008 |Injection of steroid into joint (procedure)| has Direct substance (attribute) of Steroid (substance)

<figure><img src="../../../../../../.gitbook/assets/image (26).png" alt=""><figcaption><p>Stated view of 231274008 |Injection of steroid into joint (procedure)| with Direct substance (attribute) of Steroid (substance)</p></figcaption></figure>

{% hint style="warning" %}
**Pharmaceutical / biologic product**

Although Pharmaceutical / biologic product (product) and its descendants are considered valid values for the Direct substance (attribute) by the MRCM, they are not currently used as values for this attribute in the International Release. The only exception is 787859002 |Vaccine product (medicinal product)| and its descendants, which can be used as valid values for this attribute.
{% endhint %}

## Has focus

Has focus (attribute) specifies the Clinical finding or Procedure which is the focus of a procedure. This attribute is self-grouped.

For example,

* 385941006 | Wound care assessment (procedure)| Has focus of Wound care (regime/therapy)

## Has intent

The Has intent attribute is used when a procedure may be performed for various reasons, described with subtypes of 363675004 |Intents (nature of procedure values) (qualifier value)|, such as diagnostic, palliative, preventive, therapeutic, etc. These intents are not used to define procedures with intents that are inherent to the procedure; such as biopsies that are by definition diagnostic, or fracture fixations which are always therapeutic.

The Has intent attribute should be grouped with other attributes that represent the procedure with that intent.

For example,

* 108249004 | Audiologic AND/OR audiometric test including vestibular function (procedure)| is inherently diagnostic, so it would not be modeled with a Has intent (attribute) of Diagnostic intent (qualifier value).
* 274432006 | Therapeutic aspiration of ovary (procedure)| and 274389009 | Diagnostic aspiration of ovary (procedure)| are both modeled with the Has intent (attribute), as the aspiration of ovary procedure can be either therapeutic or diagnostic.

## Indirect device

Indirect device (attribute) represents action on something that is located in or on a device, but is not directly on the device itself. This attribute is infrequently needed. When modeling, carefully consider its use.

For example,

* 232762008 | Excision of vegetations from implanted mitral valve (procedure)| has Indirect device of Mitral valve prosthesis device (physical object).
  * In this example, the vegetation is being excised. The mitral valve prosthesis device is where the vegetation is located, but the mitral valve prosthesis, itself, is not excised. Thus, the mitral valve prosthesis device is the Indirect device.

## Indirect morphology

Indirect morphology (attribute) describes the morphology that is acted upon, but is not the direct object of the Method action. This means the procedure acts directly on something else, e.g., a device, substance, or anatomical structure.

For example,

* 404205006 | Removal of mesh from wound (procedure)| has Indirect morphology of Wound (morphologic abnormality)

## Method

Method (attribute) represents the action being performed to accomplish the procedure.

For example,

* 10255001 | Incision of ureter (procedure)| has Method (attribute) of Incision - action (qualifier value)

Procedures with a Method (attribute) can be described using an action verb that corresponds to the method. The direct object/s of the action verb should be represented using one or more of the four direct-object attributes, depending on whether the direct object on which the method acts is an:

* Anatomical structure: Procedure site - Direct
* Morphologic abnormality: Direct morphology
* Device: Direct Device
* Substance: Direct Substance

If the anatomical structure, device, or substance of the direct object is indeterminate, do not use the direct-object attributes.

When modeling procedures where the Method is _Removal - action_ (qualifier value) or one of its subtypes, e.g. Excision, Surgical biopsy, etc., for removal of:

* Structures, grafts, and tissue lesions (e.g., cysts, tumors, etc. are considered removal of the site), use _Procedure site - Direct._
* Devices, calculi, thrombi, foreign bodies, and other non-tissue entities from the structure, use _Procedure site - Indirect._

For example,

* 43748006 |Removal of urinary bladder catheter (procedure)| has a Method (attribute) of Removal - action (qualifier value). Because a device is being removed, use Procedure site - Indirect (attribute) with a value of Bladder and outflow structure (body structure)

Method (attribute) does not describe

* procedure approach, e.g., translumbar
* equipment, e.g., sutures
* physical force, e.g., laser energy

### Method attribute grouping

Attributes should be grouped with the Method (attribute) to which they apply. In the absence of a Method (attribute), related attributes should be grouped together.

Exception,

* Recipient category (attribute)
  * A single procedure concept should not be precoordinated when more than one Recipient Category is involved. Such complex statements should have two or more procedure concepts that are placed into an appropriately structured electronic health application.&#x20;
  * See separate attribute entry for [_Recipient category_](./#recipient-category) below.

No relationship group can contain more than one Method (attribute). If a procedure has more than one method, each Method (attribute) serves as the anchor of a separate relationship group that will contain any defining relationships that represent a direct object (and, where relevant, indirect object) of the Method's action. This is true even if the different Methods each act on the same direct object. Each relationship group can be thought of as representing a component of the procedure that involves a particular action.

## Occurrence

Occurrence (attribute) is applied to procedures during a period of life. For example, procedures related to the gravid uterus should be modeled by the combination of the occurrence of the maternal pregnancy period and the uterus.

## Priority

Priority (attribute) is used when a procedure concept specifies a priority. This attribute is self-grouped.

For example,

* 708932005 | Emergency hemodialysis (procedure)| has Priority of Emergency (qualifier value)
* 177141003 | Elective cesarean section (procedure)| has Priority of Elective (qualifier value)

260870009 | Priority (attribute)| is most often used to differentiate elective and emergency subtypes of a procedure that can be performed on either basis. With the exception of Cardiopulmonary resuscitation (procedure), this attribute is normally used only to define concepts whose FSNs specify a priority, not for modeling procedures that imply an emergency priority, such as |Heimlich maneuver (procedure)| or those that are inherently elective, such as |Augmentation mammoplasty (procedure)|.

## Procedure approach

Procedure approach (attribute) specifies the directional, relational, or spatial access to the site of a procedure. The range for 116688005 | Procedure approach (attribute)| is << 103379005 | Procedural approach (qualifier value)| .

For example,

* 33195004 |External beam radiation therapy procedure (procedure)| has Procedure approach (attribute) of External approach (qualifier value).

<figure><img src="../../../../../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

9795009 |Open reduction of orbital floor blowout fracture by periorbital approach (procedure)| has Procedure approach (attribute) of Periorbital approach (qualifier value).

<figure><img src="../../../../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

## Procedure device

Procedure device (attribute) is used to model devices associated with a procedure. This attribute is used to define high-level, general concepts that aggregate procedures according to the device involved.

Procedure device subsumes the more specific attributes, Direct Device, Indirect Device, Using Device, and Using Access Device. The more specific attributes should be used instead of Procedure Device, if possible.

For example,

* 276272002 | Catheter procedure (procedure)| has Procedure device (attribute) of Catheter, device (physical object)

{% hint style="warning" %}
**Procedure device**

The attribute values in the Procedure Device hierarchy include Device (physical object) and its descendants.

There are a limited number of drug delivery devices in SNOMED CT. These concepts descend from Drug-device combination product (product) which is a descendant of both Device (physical object) and Pharmaceutical / biologic product (product). Although they carry the hierarchy tag of (product), they are acceptable values for attributes in the Procedure Device attribute hierarchy.
{% endhint %}

## Procedure morphology

Procedure morphology (attribute) is used to specify the morphology, or abnormal structure, involved in a procedure. It is used when defining general concepts that subsume direct and indirect morphology. It subsumes the more specific attributes, Direct and Indirect Morphology. These should be used, if possible.

{% hint style="warning" %}
**Morphologically abnormal structures**

Hematoma, calculus, foreign body, blood clot, embolus, and some other morphologies are not strictly body structures. But, they are included in the body structure hierarchy under morphologically abnormal structure and are valid values for the Procedure Morphology attributes.
{% endhint %}

## Procedure site

Procedure site (attribute) describes the body site acted on or affected by a procedure. The Procedure site (attribute) is

* used to model the site for high-level grouping-type procedure concepts
* most often used for concepts that do not require a 260686004 | Method (attribute)| and 129264002 | Action (qualifier value)| pair
* not required in order for the classifier to work properly

363704007 | Procedure site (attribute)| subsumes the more specific attributes, 405813007 | Procedure site - Direct (attribute)| , which is the site _directly_ acted upon, and 405814001 | Procedure site - Indirect (attribute)| , which is the site _indirectly_ acted upon. The more specific attributes should be used if possible (see separate entries for _Procedure site - Direct_ and _Procedure site - Indirect_).

For example,

* 118839001 | Procedure on colon (procedure)| has Procedure site of Colon structure (body structure)

When modeling procedures where the Method is _Removal - action_ (qualifier value) or one of its subtypes, e.g., Excision, Surgical biopsy, etc., for removal of:

* Structures, grafts, and tissue lesions (e.g., cysts, neoplasms, abscesses, wounds, warts, aneurysms, herniations, oral clefts, etc.) are considered removal of the site, use _Procedure site - Direct._
* Devices, calculi, thrombi, foreign bodies, and other non-tissue entities from the structure, use _Procedure site - Indirect._

{% hint style="info" %}
**Procedure site**\
Procedures are not necessarily categorized by site.
{% endhint %}

### Use of Structure of vs. Entire as value of the Procedure site attributes

Structure of \<anatomical structure> rather than Entire \<anatomical structure> should be used as the value for procedure site attributes, except where the procedure FSN explicitly specified that the entire structure is the object of the procedure.

For example,

* 23968004 | Excision of colon (procedure)| has 405813007 | Procedure site - Direct (attribute)| of 71854001 | Colon structure (body structure)|
* 26390003 | Total colectomy (procedure)| has 405813007 | Procedure site - Direct (attribute)| of 302508007 | Entire colon (body structure)|

## Procedure site - Direct

Procedure site - Direct (attribute) is used when the action of the procedure is directly aimed at anatomical or acquired body structure or site, rather than something else located there (e.g., a device), i.e., when the 260686004 | Method (attribute)| is 129303008 | Removal - action (qualifier value)| or one of its subtypes (Excision, Surgical biopsy, etc.).

For example,

* 54321008 | Cardiac flow imaging (procedure)| has 405813007 | Procedure site - Direct (attribute)| of Coronary artery structure (body structure)

Tissue lesions (cysts, neoplasms, abscesses, wounds, warts, aneurysms, herniations, oral clefts, etc.) are considered part of the procedure site and should also use 405813007 | Procedure site - Direct (attribute)| .

For example,

* Repair of rectocele (procedure) has a Procedure site - Direct (attribute) of Rectum structure and a Direct morphology (attribute) of Herniated structure
* Closure of skin wound (procedure) has a Procedure site - Direct (attribute) of Skin structure and a Direct morphology (attribute) of Wound
* Fixation of fracture (procedure) has a Procedure site - Direct (attribute) of Bone structure and a Direct morphology (attribute) of Fracture

## Procedure site - Indirect

Procedure site - Indirect (attribute) specifies the anatomical location but is not the direct focus of the procedure. The direct object of the action may be a device, a substance, or a morphologic abnormality that is not a part of the tissue structure of the anatomical site in which it is located, such as a calculus, thrombus, or foreign body. Thus, 405814001 | Procedure site - Indirect (attribute)| is typically found in a relationship group with a second, "direct" attribute-value relationship, such as a Direct morphology, Direct substance, or Direct device.

For example,

*   405433000 | Removal of catheter from brachial vein (procedure)| has:

    * Method of Removal - action (qualifier value)
    * Procedure site - Indirect of Structure of brachial vein (body structure)
    * Direct device of Venous catheter (physical object)

    <figure><img src="../../../../../../.gitbook/assets/image (29).png" alt=""><figcaption><p>Stated view of 405433000 |Removal of catheter from brachial vein (procedure)|</p></figcaption></figure>



* 371005009 | Removal of calculus of urinary bladder (procedure)| has:
  * Direct morphology of Calculus (morphologic abnormality)
  * Method of Removal - action (qualifier value)
  * Procedure site - Indirect of Urinary bladder structure (body structure)

<figure><img src="../../../../../../.gitbook/assets/image (30).png" alt=""><figcaption><p>Stated view of 371005009 |Removal of calculus of urinary bladder (procedure)|</p></figcaption></figure>

## Recipient category

Recipient category (attribute) specifies the type of individual or group upon which the action of the procedure is performed.

For example,

* 105455006 | Donor for medical or surgical procedure (person)| has Recipient Category (attribute) of Donor if the subject of the record is the Blood product donor (person).

This can be used in blood banking procedures to differentiate the donor vs the recipient of blood products.

{% hint style="warning" %}
**Recipient category**

Recipient category is not used for a procedure where the subject of the procedure is someone other than the subject of record.
{% endhint %}

## Revision status

Revision status (attribute) refers to another procedure performed on the same site for the same condition. A procedure without a revision status is considered to be performed for the first time. A revision procedure can be modeled with a Revision status (attribute) of Revision - value (qualifier value).

For example,

* 128323000 | Revision of implant (procedure)| has a Revision status (attribute) of Revision - value (qualifier value)

## Route of administration

_Route of administration_ represents the route by which a procedure introduces a substance into the body. The range involves subtypes of 284009009 |Route of administration value (qualifier value)|. When using this attribute, an additional attribute of |Procedure site - indirect| should be modeled and grouped with the |Route of administration (attribute)|.

For example,

* 410572008 | Injection of steroid via intravitreal route (procedure)| has the | Route of administration (attribute)| of Intravitreal route (qualifier value)

<figure><img src="../../../../../../.gitbook/assets/image (31).png" alt=""><figcaption><p>Stated view of 410572008 |Injection of steroid via intravitreal route (procedure)|</p></figcaption></figure>

While the values for |Procedure site - Indirect| and |Route of administration| attributes may be similar and seem redundant, their presence is necessary for consistent subsumption.

Examples of complementary values of Route of administration and Procedure site - Indirect

| Route of administration (qualifier value) | Body structure value of Procedure site - Indirect |
| ----------------------------------------- | ------------------------------------------------- |
| Intravenous route                         | Venous structure                                  |
| Oral route                                | Mouth region structure                            |

## Using access device

Using access device (attribute) specifies the instrument or equipment used to access the site of a procedure.

For example,

* 274323008 | Endoscopic biopsy of colon (procedure)| has a Using access device (attribute) of Colonoscope, device (physical object)

### Endoscopes

Many procedures can be carried out using tools attached to or operated via channels within the endoscope. In some cases the device IS used for access (such as endoscopy of the GI tract), e.g. ERCP in particular allows you to both visualize and operate upon the sphincter of Oddi/ampulla of Vater using cutting devices (knives or wires etc.) and then passing a basket up into the CBD to remove stones. The correct attribute for the device is |Using access device (attribute)|.

## Using device

Using device (attribute) refers to the instrument or equipment utilized to execute an action. It is used when the device is actually used to carry out the action, that is the focus of the procedure. If the device is simply the means to access the site of the procedure, then _Using access device_ is the appropriate attribute.

For example,

* 51064005 | Core needle biopsy of larynx (procedure)| has a Using device (attribute) of Core biopsy needle, device (physical object)

### Endoscopes

When an Incision role group is included in the concept model, then |Using device| attribute is appended to the Inspection role group. For example, access to either the abdominal cavity or a joint capsule is achieved by an ordinary incision using a scalpel blade. The laparoscope or arthroscope is then introduced into the cavity through the incision, i.e. the endoscope is not the _access_ device.

## Using energy

Using energy (attribute) refers to the energy used to execute an action.

For example,

* 65952009 | Gamma ray therapy (procedure)| has Using energy of Gamma radiation (physical force)

## Using substance

Using substance (attribute) describes the Substance used to execute the action of a procedure. It is not the substance on which the procedure's method directly acts, the Direct substance.

For example,

* 285754008 | Contrast radiography of esophagus (procedure)| has Using substance of Contrast media (substance)

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Procedure%20Attributes" class="button primary">Provide Feedback</a>
