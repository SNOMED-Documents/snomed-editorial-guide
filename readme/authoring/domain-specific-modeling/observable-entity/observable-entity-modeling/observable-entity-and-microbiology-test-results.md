---
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: false
  tags:
    visible: true
  actions:
    visible: true
  anchors:
    visible: true
---

# Observable Entity and Microbiology Test Results

When microbiology laboratory results are encoded, it is important to be aware of the context provided by the observation, i.e., the test performed and, therefore, the implied meaning of the result value, i.e., the organism.

For example, the combination of _Logical Observation Identifiers Names and Codes (LOINC)_ for the lab test and _SNOMED CT_ for the organism, provides a unique and specific meaning:

* LOINC provides microbiology reporting codes with attributes including the _property_ through the use of _PRID_ (presence or identity) and the _scale_ through the use of _NOM_ (nominal or categorical response that does not have a natural ordering) as the result value (typically the name of organism).
  * Use of organism concepts in combination with such LOINC codes implies that a specific organism is seen, detected, identified, isolated, or present.

{% hint style="warning" %}
**Organism**

On its own, an organism concept can only indicate the definition of that organism. Its detection or presence can only be implied when it is paired with other information that may come from the electronic health application and/or from the LOINC observation.
{% endhint %}

## Organism X or organism Y

Use organism X or organism Y when a laboratory report indicates a single isolate is assumed, but the lab is unable (for any reason) to differentiate the result instance.

* For example,
  * 703015006 | Human coxsackievirus or human echovirus (finding)|

For bacteria, these findings are subtypes of 1418134004 |Bacteria finding (finding)|.

## Organism X, not organism Y

Use organism X, not organism Y when a laboratory report indicates a class of organisms described by the exclusion of specific Linnaean or non-Linnaean classes. These concepts are found in the organism hierarchy (based on reasonable use cases to avoid a combinatorial explosion). They are a primitive super class, in between the species or species subtype.

* For example,
  * 115407004 | Haemophilus influenzae, not b (organism)|

#### Exception

The common term _yeast_ can refer to two separate classes: 1) a morphologic form of a dimorphic fungus; or 2) an organism in kingdom Fungi that is truly a yeast. Therefore, while the super class _yeast_ is represented as an organism, “X, not organism Y” type concept is represented in the clinical finding hierarchy (as descendant of 769070007 |Yeast detected (finding)|) since one potential meaning of use is a diagnostic morphologic form of an organism rather than an organism itself.

* For example,
  * 769071006 | Yeast not Candida albicans detected (finding)|

## Genus X, not species Y and not species Z

Use Genus X, not species Y and not species Z when a laboratory report indicates a species of Genus X and confirms that it is not species Y, nor species Z. E.g. Bacillus species, not Bacillus anthracis and not Bacillus cereus (organism).

Use this naming convention only with Genus, species, and subspecies levels of the hierarchy.

## _Untypable_ organisms

Laboratory reports and journal articles may include an organism that could not be serotyped, e.g. E. _coli, untypable_. The requests for such concepts are declined due to ambiguity.  Instead, use the closest taxonomic level in the hierarchy.

## Presumptive values

Laboratory findings may be reported with a status of preliminary, presumptive, provisional, etc. These typically cover reportable or notifiable lab values. The status of a report is different from the result; it is part of the electronic health application model/message. The requests for such concepts are declined as they are ambiguous and subject to limitless combinations.

{% hint style="warning" %}
**Concepts with presumptive values**

Existing concepts with presumptive values are undergoing review for inactivation.
{% endhint %}

## Mixed Organism

Some laboratories report findings indicating a mixed population of bacteria from several classes, e.g., _mixed anaerobic Gram negative bacilli_. The request for such a concept is added as a _clinical finding._ The actual organism is unknown; however, there is a result, although more general.

## Bacterial phenotype findings

A bacterial phenotype observed in a specimen or isolate, e.g., cell shape, arrangement or Gram stain reaction, is represented as a clinical finding. This guidance applies to bacteria.

The FSN of the finding names the phenotype only and does not include _present_ or _absent_, e.g., 1411589003 |Bacilli finding (finding)|.

These findings are not used as result values for microbiology tests, and the range of |Has interpretation (attribute)| does not include clinical findings.

The finding is defined using a phenotype-specific observable entity (Interprets) and a qualifier value (Has interpretation). Each phenotype axis has its own observable entity, e.g., Bacterial morphology, Bacterial arrangement and Gram stain reaction.  A single observable entity must not span more than one axis. The qualifier values are children of 260245000 |Finding value (qualifier value)|, as required by the MRCM range for |Has interpretation|.

Where several phenotype axes are reported together, a precoordinated clinical finding is used rather than a separate observable and value for each axis.

For example, see the stated form of 734445005 |Gram-positive bacilli in chains (finding)|:

<figure><img src="../../../../../.gitbook/assets/Screenshot 2026-11-06 at 12.35.33 PM.png" alt=""><figcaption></figcaption></figure>

## Reporting Negative and Positive Results

Laboratories perform and report on specific tests to identify the absence, as well as the presence, of a particular pathogenic organism. Laboratories typically report negative result values, such as _X not seen_, _X not detected,_ X _not isolated_, and _no X seen (or identified or isolated)_ and positive results as X _seen_, X _detected_, and X _isolated_. The following tables includes the acceptable modeling for negative and positive results.

**Microbiology Tests: Reporting of Negative and Positive Values with Examples**

<table data-header-hidden><thead><tr><th width="134.58203125">Microbiology Tests: Reporting of Negative and Positive Values with Examples</th><th width="247.0078125"></th><th width="365.8515625"></th><th width="327.88671875"></th></tr></thead><tbody><tr><td><strong>Lab test type (Observation)</strong></td><td><strong>Result value</strong></td><td><strong>Example lab test (e.g. SNOMED CT and/or LOINC term)</strong></td><td><strong>Example result value</strong></td></tr><tr><td>General culture (where implied scale = nominal)</td><td><p>No X isolated (finding)</p><p>X (organism)</p></td><td><p>61594008 |Microbial culture (procedure)|</p><p>11475-1 |Microorganism identified in Unspecified specimen by Culture</p></td><td><p><strong>Valid value</strong></p><p>168204005|Salmonella not isolated (finding)|</p><p>27268008|Genus Salmonella (organism)|</p><p><strong>Invalid value</strong></p><p>264887000 |Not isolated (qualifier value)</p><p>| 46651001 |Isolated (qualifier value)|</p></td></tr><tr><td>Organism Specific culture</td><td>Not isolated (qualifier value) Isolated (qualifier value)</td><td><p>122206002 |Bordetella pertussis culture (procedure)|</p><p>48741-3 |Bordetella pertussis; Nasopharynx; Culture</p></td><td><p><strong>Valid value</strong></p><p>264887000|Not isolated (qualifier value)| 46651001|Isolated (qualifier value)|</p><p><strong>Invalid value</strong></p><p>Bordetella pertussis not isolated Bordetella pertussis isolated</p></td></tr><tr><td>General microscopic testing (where implied scale = Nominal)*</td><td><p>No X seen (finding)</p><p>X (organism)</p></td><td><p>609009000 |Microscopic examination of bacterial smear of urine specimen (procedure)|</p><p>25145-4 |Bacteria [Presence] in Urine sediment by Light microscopy</p></td><td><p><strong>Valid value</strong></p><p>27268008|Genus Salmonella (organism)|</p><p><strong>Invalid value</strong></p><p>47492008 |Not seen (qualifier value)|</p></td></tr><tr><td>Specific microscopic testing</td><td>Not seen (qualifier value) Present (qualifier value)</td><td>408215009 |Cryptosporidium microscopy (procedure)|</td><td><p><strong>Valid value</strong></p><p>47492008|Not seen (qualifier value)| 52101004|Present (qualifier value)|</p><p><strong>Invalid value</strong></p><p>No Cryptosporidium seen Cryptosporidium seen</p></td></tr><tr><td>Serologic, DNA or other organism specific test</td><td><p>Not detected (qualifier value) Detected (qualifier value)</p><p>Rationale: Almost all of these tests are organism-specific</p></td><td><p>871555000 |Detection of ribonucleic acid of Severe acute respiratory syndrome coronavirus 2 (observable entity)|</p><p>95406-5 |SARS-CoV-2 (COVID-19) RNA [Presence] in Nose by NAA with probe detection</p></td><td><p><strong>Valid value</strong></p><p>260415000|Not detected (qualifier value)|</p><p>260373001|Detected (qualifier value)|</p><p><strong>Invalid value</strong></p><p>No Severe acute respiratory syndrome coronavirus 2 detected</p><p>Severe acute respiratory syndrome coronavirus 2 detected</p></td></tr></tbody></table>

\*Where a microscopic test identifies only the phenotype of the organism, a phenotype-defined organism grouper can be used as the result value, e.g., with 365971000119107 | Identification of organism in smear by Gram stain (observable entity)| could have a result of 83514008 |Gram-positive bacillus (organism)|. Clinical findings of the kind described under [Bacterial phenotype findings](observable-entity-and-microbiology-test-results.md#bacterial-phenotype-findings) are not used as result values.

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Observable%20Entity%20and%20Microbiology%20Test%20Results" class="button primary">Provide Feedback</a>
