# Infectious vs. inflammatory

Disorders with the suffix "-itis" (e.g., cystitis, prostatitis, tonsillitis, appendicitis) are often infectious as well as inflammatory in nature.

For inflammatory conditions whose FSNs specify an _infective_ _cause_ , the modeling should include:

* |Causative agent (attribute)| with the specified organism
* |Pathological process (attribute)| with the type of infectious process
* |Associated morphology (attribute)| with Inflammatory morphology or subtype
* |Finding site (attribute)| with a body structure when known

For inflammatory conditions whose FSNs do _not_ specify an infective cause, an infectious cause should neither be assumed nor modeled when the FSN does not specify it. The modeling would then exclude a Causative agent and Pathological process and should include only:

* |Associated morphology (attribute)| of Inflammatory morphology or subtype
* |Finding site (attribute)| with a body structure when known

Example of inflammatory _and_ infectious disorder,

441551009 |Inflammation of larynx caused by virus (disorder)| (synonym, Viral laryngitis) includes a |Causative agent (attribute)| of |Virus (organism)| and a |Pathological process (attribute)| of |Infectious process (qualifier value)|.

<figure><img src="../../../../../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../../authoring/clinical-finding-and-disorder/images/174690497.png" alt=""><figcaption><p>Figure: Stated view of 441551009 |Inflammation of larynx caused by virus (disorder)|</p></figcaption></figure>

Example of inflammatory disorder _not_ specified as infectious,

446292002 |Necrotizing inflammation of lymph node (disorder)| (synonym, Necrotizing lymphadenitis) does not specify an infective cause, so it is neither modeled with Causative agent nor Pathological process. The model contains an |Associated morphology (attribute)| and a |Finding site (attribute)|.

<figure><img src="../../../../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../../authoring/clinical-finding-and-disorder/images/174690496.png" alt=""><figcaption><p>Figure: Stated view of 446292002 |Necrotizing inflammation of lymph node (disorder)|</p></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Infectious%20vs.%20inflammatory" class="button primary">Provide Feedback</a>
