# Vaccine needed

The need for a vaccination is represented as a _situation with explicit context_, not as a clinical finding. New requests are created as subtypes of 122541000119104 |Vaccination needed (situation)| and modeled as follows:

| Attribute                                              | Value                                                                                                |
| ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| 363589002 \|Associated procedure (attribute)\|         | <127785005 \|Administration of substance to produce immunity, either active or passive (procedure)\| |
| 408730004 \|Procedure context (attribute)\|            | 410525008 \|Needed (qualifier value)\|                                                               |
| 408732007 \|Subject relationship context (attribute)\| | 410604004 \|Subject of record (person)\|                                                             |
| 408731000 \|Temporal context (attribute)\|             | 410512000 \|Current or specified time (qualifier value)\|                                            |

FSN pattern: <_Vaccine> vaccine needed (situation)_

For example,

* FSN: Influenza vaccine needed (situation)
* PT: Influenza vaccine needed

The associated procedure value must be an active subtype of 127785005 |Administration of substance to produce immunity, either active or passive (procedure)|. If no suitable procedure exists, it is requested before the situation concept is created.
