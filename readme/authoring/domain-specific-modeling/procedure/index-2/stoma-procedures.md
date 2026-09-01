# Stoma procedures

A distinction is needed between stoma procedures and procedures where an anastomosis is created between two hollow organs.&#x20;

A stoma is a surgically created opening connecting an internal body structure to the external skin surface. Although most commonly formed on the abdominal wall, stomas can be created at other anatomical sites, such as the neck (tracheostomy) or perineum (perineal urethrostomy). The defining criterion is cutaneous externalization.&#x20;

In contrast, internal anastomoses between two visceral structures, such as an entero-enterostomy or ureterointestinal anastomosis, while often referred to as _internal stomas_ are not classified as stomas, as they lack cutaneous communication or exteriorization.

The morphologies resulting from these two different types of procedures may both be termed using the suffix _ostomy_, but they mean different things:

* For example,
  * 272726003 |Gastrostomy (morphologic abnormality)| refers to the result of the exteriorization of the stomach through the abdominal wall.
  * 264022007 |Ileocolostomy anastomosis (morphologic abnormality)| refers to the anastomosis between the ileon and the colon.

{% hint style="danger" %}
These two different types of morphologies were formerly termed _external stomas_ and _internal stomas_. Procedures and Morphologic abnormalities named _internal_ and/or _external stoma_ are no longer allowed in SNOMED CT.
{% endhint %}

## Naming&#x20;

FSN:  X -ostomy (procedure)

PT:  X -ostomy

Acceptable SYN:

* Construction of X -ostomy
* Construction of stoma of x \<body structure>
* Construction of X \<body structure> stoma

For example,&#x20;

* FSN:  Colostomy (procedure)
* PT: Colostomy
* SYN:  Construction of colostomy

For the FSN, the terms _construction_, _creation_, and _formation_ are not allowed.&#x20;

The term _construction_ can be used for Acceptable synonyms.

#### Combination of procedures

When the FSN states a combination of procedures, the concept is termed using the conjunction “with”.&#x20;

* For example,
  * 89642006 |Anterior resection of rectum with colostomy (procedure)|
  * 307658004 |Sigmoid colectomy with colostomy (procedure)|

When an FSN states the combination of more than two procedures, use the conjunction “with” for the first two procedures, and use the conjunction “and” for the third procedure.&#x20;

* For example,
  * 44751009 |Total abdominal colectomy with proctectomy and continent ileostomy (procedure)|

#### Closure of stoma

FSN:  Closure of x \<body structure>-ostomy

PT:  Closure of x \<body structure>-ostomy

Acceptable SYN:&#x20;

* Closure of stoma of x \<body structure>
* Take-down of x stoma&#x20;
* Take-down of stoma of x \<body structure>

For example,&#x20;

* FSN:  Closure of gastrostomy (procedure)
* PT:  Closure of gastrostomy
* SYN:  Closure of stoma of stomach
* SYN:  Surgical closure of gastrostomy
* Take-down of stoma of stomach

## Modeling

### Stoma procedures without statement of the exteriorization site

Role group:&#x20;

* 260686004 |Method (attribute)| = 129354008 |Exteriorization - action (qualifier value)|
* 405813007 |Procedure site - Direct (attribute)| = < 123037004 |Body structure (body structure)|
* 363700003 |Direct morphology (attribute)| = << 245857005 |Stoma (morphologic abnormality)|

For example,&#x20;

<img src="../../../../../.gitbook/assets/unknown (5).png" alt="" height="245" width="624">



### Stoma procedures with stated exteriorization site

Role group:&#x20;

* 260686004 |Method (attribute)| = 129354008 |Exteriorization - action (qualifier value)|
* 405813007 |Procedure site - Direct (attribute)| = < 123037004 |Body structure (body structure)|
* 363700003 |Direct morphology (attribute)| = << 245857005 |Stoma (morphologic abnormality)|
* 116688005 |Procedure approach (attribute)| = < 103379005 |Procedural approach (qualifier value)|

For example,

<img src="../../../../../.gitbook/assets/unknown (6).png" alt="" height="279" width="624">

{% hint style="info" %}
Surgically created internal anastomoses or connections between two internal organs are not considered for this guidance as they are part of another hierarchy.
{% endhint %}

### Closure of stoma

Role group:&#x20;

* 260686004 |Method (attribute)| = 129357001 |Closure - action (qualifier value)|
* 405813007 |Procedure site - Direct (attribute)| = < 123037004 |Body structure (body structure)|
* 363700003 |Direct morphology (attribute)| = << 245857005 |Stoma (morphologic abnormality)|

For example,&#x20;

<img src="../../../../../.gitbook/assets/unknown (7).png" alt="" height="255" width="624">

