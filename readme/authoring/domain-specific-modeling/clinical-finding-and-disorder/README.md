# Clinical Finding and Disorder

<table><thead><tr><th width="132.0546875">Hierarchy</th><th width="271.7578125">Definition</th><th>Example</th></tr></thead><tbody><tr><td>Clinical finding</td><td>Nnormal/abnormal observations, judgments, or assessments of patients</td><td>167222005 | Abnormal urinalysis (finding) |</td></tr><tr><td>Disorder</td><td>Always and necessarily an abnormal clinical state</td><td>39579001 | Anaphylaxis (disorder) |</td></tr></tbody></table>

Clinical findings or observations are the active acquisition of subjective or objective information from a primary source. This includes information acquired from human observers, through recording of data via the use of scientific instruments, or indirectly from samples taken from the source, and evaluated separately.

#### Context

The default context for a _Clinical finding_ concept is:

* Present (vs. being absent)
* Subject of the record (the patient)
* Current, if not specifically stated or specified to a time in the past by an entity linked to the concept

{% hint style="warning" %}
The term _observations_ should not be confused with _Observable entity._ Observable entity is the name of something that can be observed and represents a question or assessment (e.g. |systolic blood pressure|, |color of iris|, |gender|) which can produce an answer or result.
{% endhint %}

The _Clinical finding_ hierarchy contains the subhierarchy of _Disorder_. Concepts that are descendants of _Disease (disorder)_ are always and necessarily abnormal clinical states. The Disease subtype allows diseases to be subtypes of other disorders, as well as subtypes of findings.

Concepts with a semantic tag of _disorder_ , must have a parent of Disease (disorder) or subtype of Disease (disorder).

* For example,
  * 95617006 | Neonatal cyanosis (disorder)| has the parent, Disease (disorder). Neonatal cyanosis is also a subtype of 3415004 | Cyanosis (finding)|

The distinction between a disorder and a finding may be difficult to define. There are, however, distinct characteristics of each.

#### Disorder vs Finding

<table><thead><tr><th width="117.6953125">Hierarchy</th><th>Characteristics</th></tr></thead><tbody><tr><td>Disorder</td><td><p>-Always and necessarily abnormal</p><p>-Necessarily have an underlying pathological process</p><p>-Have temporal persistence (may be under treatment, in remission, or inactive, even though they are still present)</p><p>-May be present as a propensity for certain abnormal states to occur, even when treatment mitigates or resolves those abnormal states</p></td></tr><tr><td>Finding</td><td><p>-May be normal (but not necessarily)</p><p>-May exist only at a single point in time (e.g. a serum sodium level)</p><p>-Cannot be temporally separate from the observation (one cannot observe them and say they are absent, nor can they be present when they cannot be observed)</p><p>-Cannot be defined only in terms of an underlying pathological process that is present, when the observation itself is not present</p></td></tr></tbody></table>

In some cases the disease process is irrefutable, e.g., meningococcal meningitis. In others an underlying disease process is assumed based on the temporal and causal association of the disorder and its manifestation, e.g., nystagmus (disorder) is different from nystagmus present (finding). Nystagmus present (finding) may be a normal physiological response to head rotation. A person who spins around and has nystagmus present (finding), does not have nystagmus (disorder). Alternatively, a person may have nystagmus (disorder), but not nystagmus present (finding), i.e., they do not currently manifest nystagmus. Similarly, hearing loss (disorder) is different from perception of hearing loss (finding), which can be due to a number of temporary causes, such as excessive ear wax.

## Topics in this section

{% content-ref url="clinical-finding-attributes-summary.md" %}
[clinical-finding-attributes-summary.md](clinical-finding-attributes-summary.md)
{% endcontent-ref %}

{% content-ref url="clinical-finding-defining-attributes.md" %}
[clinical-finding-defining-attributes.md](clinical-finding-defining-attributes.md)
{% endcontent-ref %}

{% content-ref url="index/" %}
[index](index/)
{% endcontent-ref %}

{% content-ref url="clinical-finding-and-disorder-modeling/" %}
[clinical-finding-and-disorder-modeling](clinical-finding-and-disorder-modeling/)
{% endcontent-ref %}







<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=SCT+Editorial+Guide&entry.670899847=Clinical%20Finding%20and%20Disorder" class="button primary">Provide Feedback</a>
