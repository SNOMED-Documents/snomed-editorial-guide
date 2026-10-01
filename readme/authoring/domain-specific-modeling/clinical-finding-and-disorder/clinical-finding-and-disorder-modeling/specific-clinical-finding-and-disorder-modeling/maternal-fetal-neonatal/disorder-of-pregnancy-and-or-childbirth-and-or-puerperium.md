# Disorder of Pregnancy and/or Childbirth and/or Puerperium

The following principles were utilized during the 2026 inactivation and remodeling of concepts within the hierarchies 198609003 |Complication of pregnancy, childbirth and/or puerperium (disorder) and 362972006 |Disorder of labor / delivery (disorder).&#x20;

## Temporal Semantics

The modeling of concepts whose FSNs contain certain words have been standardized by a consistent specified temporal value (with occasional exceptions) as tabulated below:

<table data-header-hidden><thead><tr><th width="140.865234375"></th><th width="238.5546875"></th><th></th></tr></thead><tbody><tr><td><strong>Phrase</strong></td><td><strong>Default temporal value</strong></td><td><strong>Notes</strong></td></tr><tr><td>‘Obstetric’</td><td>Maternal antenatal and/or intrapartum and/or postpartum period</td><td>Occasionally, a published FSN prompts using a more restricted temporal period, e.g., 397752008 |Obstetric perineal wound disruption (disorder)<br></td></tr><tr><td>‘Pregnancy’</td><td>Maternal antenatal and/or intrapartum period</td><td>Pregnancy is defined as the unity of the mother and fetus at the point of conception until the end of the third stage of labor. Occasionally, exception occurs where a condition is commonly referred to as ‘pregnancy’ related, but extends beyond birth, e.g., 10749871000119100 |Malignant neoplastic disease in pregnancy (disorder)</td></tr><tr><td>‘Delivery’</td><td>Maternal intrapartum period</td><td>Occasionally, the notion of delivery is more specific, relating only to the ‘delivery of the fetus’ and excluding the third stage of labor, e.g., 1343000 |Deep transverse arrest (disorder)</td></tr><tr><td>‘Childbirth’</td><td>Maternal intrapartum period</td><td>The use of ‘childbirth’ is inconsistent historically and can sometimes be used more generally to include the antenatal period, as well as the intrapartum period and/or postpartum, e.g., 717816002 |Infection of nipple associated with childbirth with attachment difficulty (disorder)</td></tr><tr><td>‘Postpartum’</td><td>Maternal postpartum period</td><td>Synonymous with puerperal and describes the six week phase commencing at the end of the third stage of labor.</td></tr></tbody></table>

## Variants of Complication

The notion of _complication_ is explicitly stated in legacy material from ICD to refer to ‘adverse evolution’.  The existing descendants of |Complication of pregnancy, childbirth AND/OR puerperium (disorder)| were incomplete and predominantly related to maternal disorders but also historically included a small number of fetal concepts affected by the maternal environment. For these reasons, the following concepts have been inactivated as ambiguous with historical association to their respective separate maternal and fetal grouping superordinates:

* 198609003 |Complication of pregnancy, childbirth and/or puerperium (disorder)|
* 609496007 |Complication occurring during pregnancy (disorder)|
* 199745000 |Complication occurring during labor and delivery (disorder)|

Combined high level maternal and fetal grouping concepts, e.g., Maternal disorder and/or fetal disorder during intrapartum period, have not been added, as these coalesced classes can be located  using Expression Constraint Language (ECL).

## X complicating Y

High level general concepts, e.g., 45828008 |Anemia in mother complicating pregnancy, childbirth AND/OR puerperium (disorder), have been inactivated as ambiguous with historical association to an explicit concept relating to the presence of the condition that does not state that it is _complicating_, for example, |Maternal anemia during antenatal and/or intrapartum and/or postpartum period|.&#x20;

In contrast, where the word _complicating_ has been applied to a more limited time phase, e.g., 10742121000119104 |Asthma in mother complicating childbirth (disorder), this concept has been retained, as potentially clinically valuable, but marked as incompletely defined (primitive) due to the notion’s inherent lack of specificity.  In this exemplar, 10742121000119104 |Asthma in mother complicating childbirth (disorder), could denote the co-occurrence and impact of asthma on labor but the nuance is not explicit, and the notion could also involve the exacerbation of asthma secondary to the process of labor (or, of course, both interactions could be present). Thus, ‘Asthma in mother complicating childbirth’ is semantically more complex than the simple co-occurrence of ‘asthma with childbirth’ and consequently the concept has to be primitive, as the word _complicating_ here captures the ‘adverse evolution’ of certain conditions away from the _norm_ in the intrapartum state.&#x20;

## Y complicated by X&#x20;

Concepts such as 34270000 |Miscarriage complicated by shock (disorder) describe the occurrence of shock in the context of a miscarriage, i.e., the shock would not have occurred without the miscarriage; consequently, such concepts have been inactivated and replaced by new concepts, for example, |Shock due to miscarriage|.  It is worth noting that no further temporal information is available in the terming as to whether the shock occurred during and/or after the miscarriage.

## Variants of _Affecting Pregnancy_ and _Affecting Management_

Concepts with FSNs such as ‘X affecting pregnancy’ and ‘Y affecting management of pregnancy’ have been inactivated and replaced with explicit concepts of the form: |Disorder of pregnancy due to X|

* For example,
  * 443006 |Cystocele affecting pregnancy (disorder) has been inactivated with historical association to a new concept 1381656002 |Maternal cystocele during antenatal and/or intrapartum period (disorder)
  * 106008001 |Delivery AND/OR maternal condition affecting management (disorder) has been inactivated with historical association to 1269075002 |Maternal disorder during intrapartum period (disorder)

## Ectopic Pregnancy

The occurrence value for ectopic pregnancy concepts have been defined as _Maternal antenatal period_ with an associated finding site of |Structure of product of conception|. Where the ectopic is explicitly a fetus, this has also been modeled.  For example, 237253003 |Viable fetus in abdominal pregnancy (disorder) is modeled as relating to the abdomen within the maternal antenatal period & the fetus in relation to the fetal period, (as, in this case, a viable fetus is a fetal disorder as well as an abdominal pregnancy). The conceptus is an embryo until the end of the eighth week of pregnancy, and from the beginning of the ninth week until delivery, the conceptus is known as the fetus. The first trimester begins at conception until the end of week 12, so this includes the transition between embryo and fetus at the end of 8 weeks gestation.&#x20;

An ectopic pregnancy is also defined as NOT being within the uterine cavity, but being located in the abdominopelvic cavity or a substructure.  Consequently, 198627000 |Angular pregnancy (disorder)|, which is intrauterine, is NOT considered an ectopic pregnancy.  Where the site of the ectopic is stated, e.g., 79586000 |Tubal pregnancy (disorder)|, this is modeled with the finding site |Fallopian tube| and an occurrence of |Maternal antenatal period|.

## Miscarriage and Abortion

Concepts relating to miscarriage and abortion are both modeled using a finding site of |Structure of product of conception| and an occurrence of |Maternal antenatal period|, e.g., 59363009 |Inevitable abortion (disorder).

## Disorders of Extra Amniotic Structures

The hierarchy 314908006 |Extra-embryonic structure (body structure)| includes:&#x20;

* 34863009 |Decidua structure (body structure)
* 78067005 |Placental structure (body structure)
* 74439004 |Chorionic structure (body structure)
* 70847004 |Structure of amnion (body structure)
* 26190007 |Yolk sac structure (body structure) (This structure is not part of the fetus, although it is attached to it).&#x20;

Disorders of extra-embryonic structures excluding the umbilical cord, e.g., placenta, necessarily relate to the Maternal antenatal/intrapartum/postpartum period, as for example, conditions such as ‘uterine retained products of conception’ extend beyond the end of the third stage of labor and persist into the postpartum period. Other disorders, e.g., 36813001 |Placenta previa (disorder)| relate to only the Maternal antenatal and/or intrapartum time period.

Disorders of the umbilical cord necessarily relate to the fetus and/or neonate.  Some concepts also relate to the maternal antenatal and intrapartum temporal period, where the pathogenesis of the connecting structure necessarily impacts on the maternal _actor_, e.g., 270500004 |Prolapsed cord (disorder). Disorders of cord during the postpartum period are modeled with only |Neonatal period|.

## Hypertension

The maternal hypertension hierarchy encompasses all concepts representing hypertension present during the antenatal, intrapartum, or postpartum periods.  It includes both conditions arising during pregnancy (such as eclampsia) and pre-existing hypertensive conditions. &#x20;

Legacy concepts and concepts with redundant phrasing have been updated as follows:

* Hypertension in obstetric context: The legacy concept 367390009 |Hypertension in the obstetric context (disorder) has been treated as synonymous with maternal hypertension and inactivated as a duplicate of 288250001 |Maternal hypertension (disorder).
* Chronic hypertension in pregnancy: The legacy phrase _chronic hypertension_ in pregnancy is considered equivalent to pre-existing hypertension.  Consequently, 8762007 |Chronic hypertension in obstetric context (disorder)| has been inactivated with historical association to a new concept 1373659007 |Pre-existing hypertension during maternal antenatal and/or intrapartum and/or postpartum period (disorder).

## Dystocia

During revisions the working definition used for labor dystocia is: an “abnormal” labor progression during the latent (up to 4-6 cm dilation) or active phase (from 4-6 cm until full dilation) of the first stage of labor; or, during the second stage (from complete cervical dilation until delivery of the baby) - this dystocia can be caused by a variety of etiologies including: uterine, pelvic (passage), and fetal origins. Pre-existing hierarchies for 31805001 |Fetal disproportion (disorder)| and 237256006 |Disorder of pelvic size and disproportion (disorder)| have been harmonized with related clinical findings rationalized to align with the following definitions:

* **Fetal orientation**: the relationship of the fetus to the uterus, cervix, and maternal pelvis.
* **Fetal presentation:** the part of the fetus occupying the lower pole of the uterus, or presenting to the pelvic inlet, e.g. vertex (cephalic), face, brow, breech, shoulder, funic (umbilical cord), or compound (more than one part, such as shoulder and hand).
* **Fetal position**: the relation of the presenting part to an anatomic axis e.g. for vertex presentation this may be occipitoanterior, occipitoposterior or occipitotransverse.
* **Fetal lie**: the relation of the fetus to the long axis of the uterus e.g. longitudinal, oblique, or transverse.

The orientation of a fetus may be determined during the pregnancy by palpation, ultrasound, etc., and these are _findings_, as the presentation, position, and lie are initially changeable until gradually becoming more set as the pregnancy approaches term.  It is at the later stages of pregnancy or during labor that the description of the fetus’ orientation relate to a _disorder._  This can become confusing ontologically.  For example, a _transverse lie_ during pregnancy is not uncommon, and although it may be indicative of an associated condition, e.g., placenta previa, it can be a normal variant.  _Transverse lie_ at a later stage of pregnancy, such as in labor, has a more significant nuance, because, not only may it be indicative of various conditions causing difficulty for the fetal head to engage, it can also be associated with an increased incidence of other conditions, such as cord prolapse.

## Isoimmunization

Concepts such as |Isoimmunization affecting pregnancy| have been inactivated as ambiguous with historical association to the maternal disorder of the development of isoimmunization secondary to incompatible (paternally-derived) fetal blood group antigens; and, the hemolytic fetal/neonatal impact:

Maternal isoimmunization has a synonym, Maternal alloimmunization.  Although alloimmunization is not strictly synonymous with isoimmunization, the terms are closely related and sometimes used interchangeably in clinical practice.  Alloimmunization refers to the immune response generated when an individual is exposed to antigens from another member of the same species (allogeneic), leading to the production of antibodies against these foreign antigens. This process commonly occurs after blood transfusion, organ transplantation, or pregnancy, and can involve a wide range of antigens, including red blood cell (RBC) antigens and human leukocyte antigens (HLA). By contrast, isoimmunization is a subset of alloimmunization, specifically describing the immune response against antigens of the same species that are genetically different but of the same type (isoantigens). In clinical usage, isoimmunization most often refers to maternal sensitization to fetal RBC antigens during pregnancy, such as Rh(D) or other blood group antigens, resulting in hemolytic disease of the fetus or newborn. Thus, _alloimmunization_ is a broader term that encompasses isoimmunization, but in the context of incompatible fetal blood group antigens, alloimmunization and Isoimmunization can be used synonymously.

There has also been considerable discussion as to the meaning of the terms _typical_, _atypical_, and _irregular_ in the context of maternal alloimmunization to incompatible fetal blood groups. Following expert consultation the following approach has been implemented:

* _typical_ and _regular_ blood group alloimmunization relates to ABO
* _irregular_ blood group alloimmunization relates to non-ABO blood group antigens

As a consequence of this, concepts relating to _atypical_ blood group antibodies have been inactivated, and a single concept 1381698004 |Maternal irregular blood group isoimmunization during antenatal and/or intrapartum period (disorder)| has been retained.

## Traumatic or Non-traumatic Injury During Pregnancy

Where injuries are explicitly traumatic and associated with the antenatal or intrapartum period, these are modeled in harmony with other domains using ‘Due to: Traumatic event’.&#x20;

Concepts with FSNs containing the notion of _damage_, e.g., 1269255003 |Damage to organ of pelvis due to incomplete miscarriage (disorder)| have been modeled as subtypes of 417163006 |Traumatic or non-traumatic injury (disorder)|. Similarly, for more specific morphologies such as _perforation_ where the etiology is also not necessarily due to a traumatic event, e.g.. 8071005 |Miscarriage with perforation of bowel (disorder), these concepts are also classified as subtypes of 417163006 |Traumatic or non-traumatic injury (disorder)|.  By contrast, other specific morphologies, including _laceration_, e.g., 7809009 |Miscarriage with laceration of uterus (disorder)|, are necessarily traumatic and are modeled with ‘Due to: Traumatic event’.

Concepts temporally relating to trauma and a procedure, e.g., 56451001 |Failed attempted abortion with perforation of broad ligament (disorder)|, are modeled as being ‘Due to: Traumatic event’ and ‘During: Termination of pregnancy (procedure)’.

Where an injury relates to a concept which explicitly states the form of delivery, this has been included in the definition, e.g., 1354495004 |Injury of urethra during vaginal delivery (disorder)| is modeled with ‘Due to: Traumatic event’ and ‘During: 700000006 |Vaginal delivery of fetus (procedure)|’.\
<br>

\
<br>
