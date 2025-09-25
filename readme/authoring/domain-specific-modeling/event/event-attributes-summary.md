# Event Attributes Summary

When authoring in this domain, these are the approved attributes and allowable ranges.&#x20;

## Domain Information for Event

| Property                      | Value                            |
| ----------------------------- | -------------------------------- |
| Domain Constraint             | << 272379006 \| Event (event) \| |
| Parent Domain                 | -                                |
| Proximal Primitive Constraint | << 272379006 \| Event (event) \| |
| Proximal Primitive Refinement | -                                |

## Author View of Attributes and Ranges for Event

| Attribute                                         | Grouped | Cardinality | In Group Cardinality | Range Constraint                                                                                                                                                                                                                                                                                                                |
| ------------------------------------------------- | ------- | ----------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 255234002 \| After (attribute) \|                 | 1       | 0..\*       | 0..1                 | << 272379006 \| Event (event) \| OR << 404684003 \| Clinical finding (finding) \| OR << 71388002 \| Procedure (procedure) \|                                                                                                                                                                                                    |
| 47429007 \| Associated with (attribute) \|        | 1       | 0..\*       | 0..\*                | << 105590001 \| Substance (substance) \| OR << 260787004 \| Physical object (physical object) \| OR << 272379006 \| Event (event) \| OR << 404684003 \| Clinical finding (finding) \| OR << 410607006 \| Organism (organism) \| OR << 71388002 \| Procedure (procedure) \| OR << 78621006 \| Physical force (physical force) \| |
| 288556008 \| Before (attribute) \|                | 1       | 0..\*       | 0..1                 | << 71388002 \| Procedure (procedure) \|                                                                                                                                                                                                                                                                                         |
| 246075003 \| Causative agent (attribute) \|       | 1       | 0..\*       | 0..1                 | << 105590001 \| Substance (substance) \| OR << 260787004 \| Physical object (physical object) \| OR << 373873005 \| Pharmaceutical / biologic product (product) \| OR << 410607006 \| Organism (organism) \| OR << 78621006 \| Physical force (physical force) \|                                                               |
| 42752001 \| Due to (attribute) \|                 | 1       | 0..\*       | 0..1                 | << 272379006 \| Event (event) \| OR << 404684003 \| Clinical finding (finding) \| OR << 71388002 \| Procedure (procedure) \|                                                                                                                                                                                                    |
| 371881003 \| During (attribute) \|                | 1       | 0..\*       | 0..1                 | << 71388002 \| Procedure (procedure) \|                                                                                                                                                                                                                                                                                         |
| 246454002 \| Occurrence (attribute) \|            | 1       | 0..\*       | 0..1                 | << 282032007 \| Periods of life (qualifier value) \|                                                                                                                                                                                                                                                                            |
| 726633004 \| Temporally related to (attribute) \| | 1       | 0..\*       | 0..\*                | << 404684003 \| Clinical finding (finding) \| OR << 71388002 \| Procedure (procedure) \|                                                                                                                                                                                                                                        |

{% hint style="info" %}
Authoring guidelines for the use of attributes in the Event hierarchy are being established.
{% endhint %}

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Event%20Attributes%20Summary" class="button primary">Provide Feedback</a>
