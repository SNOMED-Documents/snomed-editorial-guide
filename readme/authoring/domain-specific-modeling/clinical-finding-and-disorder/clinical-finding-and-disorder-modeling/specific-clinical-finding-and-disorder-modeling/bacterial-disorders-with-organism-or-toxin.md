# Bacterial disorders with organism or toxin

In modeling some bacterial disorders, there will be situations where either the organism or the toxin (substance), or both values, are required for the causative agent attribute. The decision is often determined by whether or not the bacteria are considered endotoxins or exotoxins. The most common exotoxins are:

* Botulinum Toxin
  * Enterotoxin
  * Cholera Toxin
  * Diphtheria Toxin
  * Tetanospasmin

Exotoxins are more lethal in comparison to endotoxins, but there are vaccines against many exotoxins whereas there are no vaccines against endotoxins. There can be instances where an infection is present but the disease-causing toxins are not; in this case, model the concept only with the organism and not the toxin substance.

Example,

* 276202003 |Infection caused by Clostridium tetani (disorder)| is modeled with a causative agent of 30917009 |Clostridium tetani (organism)| only.

In the situation where a disease is caused by both the infection and the associated toxin, model with both the causative agent and the toxin substance.

Example,

* 76902006 |Tetanus (disorder)| is modeled with a causative agent of 30917009 |Clostridium tetani (organism)| as well as 26159005 |Clostridium tetani toxin (substance)|.

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Bacterial%20disorders%20with%20organism%20or%20toxin" class="button primary">Provide Feedback</a>
