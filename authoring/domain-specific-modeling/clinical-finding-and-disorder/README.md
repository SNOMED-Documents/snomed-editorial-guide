# Clinical Finding and Disorder

| Definition                                                                                                                                        | Examples                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Clinical finding: normal/abnormal observations, judgments, or assessments of patients Disorder: always and necessarily an abnormal clinical state | 167222005 \| Abnormal urinalysis (finding) \| 39579001 \| Anaphylaxis (disorder) \| Clinical finding Disorder |

Clinical findings or observations are the active acquisition of subjective or objective information from a primary source. This includes information acquired from human observers, through recording of data via the use of scientific instruments, or indirectly from samples taken from the source, and evaluated separately.

The term _observations_ should not be confused with _Observable entity._ Observable entity is the name of something that can be observed and represents a question or assessment (e.g. |systolic blood pressure|, |color of iris|, |gender|) which can produce an answer or result.

The default context for a _Clinical finding_ concept is:

* Present (vs. being absent)
* Subject of the record (the patient)
* Current, if not specifically stated or specified to a time in the past by an entity linked to the concept

The _Clinical finding_ hierarchy contains the subhierarchy of _Disorder_. Concepts that are descendants of _Disease (disorder)_ are always and necessarily abnormal clinical states. The Disease subtype allows diseases to be subtypes of other disorders, as well as subtypes of findings.

Concepts with a semantic tag of _disorder_ , must have a parent of Disease (disorder) or subtype of Disease (disorder).

For example,

* ```
  * [ 95617006 | Neonatal cyanosis (disorder)|](http://snomed.info/id/95617006 "95617006 | Neonatal cyanosis \(disorder\) |") has the parent, Disease (disorder); it is also a subtype of [ 3415004 | Cyanosis (finding)|](http://snomed.info/id/3415004 "3415004 | Cyanosis \(finding\) |") . 
  ```

The distinction between a disorder and a finding may be difficult to define. There are, however, distinct characteristics of each.

| Disorder vs Finding |                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                     | Characteristics                                                                                                                                                                                                                                                                                                                                                                                       |
| Disorder            | Always and necessarily abnormal Necessarily have an underlying pathological process Have temporal persistence (may be under treatment, in remission, or inactive, even though they are still present) May be present as a propensity for certain abnormal states to occur, even when treatment mitigates or resolves those abnormal states                                                            |
| Finding             | May be normal (but not necessarily) May exist only at a single point in time (e.g. a serum sodium level) Cannot be temporally separate from the observation (one cannot observe them and say they are absent, nor can they be present when they cannot be observed) Cannot be defined only in terms of an underlying pathological process that is present, when the observation itself is not present |

In some cases the disease process is irrefutable, e.g. meningococcal meningitis. In others an underlying disease process is assumed based on the temporal and causal association of the disorder and its manifestation, e.g. nystagmus (disorder) is different from nystagmus present (finding). Nystagmus present (finding) may be a normal physiological response to head rotation. A person who spins around and has nystagmus present (finding), does not have nystagmus (disorder). Alternatively, a person may have nystagmus (disorder), but not nystagmus present (finding), i.e. they do not currently manifest nystagmus. Similarly, hearing loss (disorder) is different from perception of hearing loss (finding), which can be due to a number of temporary causes, such as excessive ear wax.

* [Clinical Finding Attributes Summary](clinical-finding-attributes-summary.md)
* [Clinical Finding Defining Attributes](clinical-finding-defining-attributes.md)
* [Clinical Finding and Disorder Naming Conventions](clinical-finding-and-disorder-naming-conventions.md)
* [Clinical finding and Disorder Modeling](clinical-finding-and-disorder-modeling.md)
