# Cardiac Valve Prosthesis Naming and Modeling

## Naming

<table><thead><tr><th width="182.86279296875"></th><th></th></tr></thead><tbody><tr><td>FSN</td><td><p>Use the following naming pattern for the FSN; align terming and case sensitivity with the FSN for the concepts selected as the attribute values, excluding the semantic tag. </p><p></p><p>[is sterile] [compositional material] [device intended site] cardiac valve prosthesis (physical object) </p><p></p><ul><li>For example, Biologic cardiac valve prosthesis (physical object) Aortic valve prosthesis (physical object)</li></ul></td></tr><tr><td>Preferred Term</td><td><p>Use the following naming pattern for the PT; align terming and case sensitivity with the PT for the concept that is selected as the attribute value. </p><p></p><p>[is sterile] [compositional material][device intended site]cardiac valve prosthesis </p><p></p><ul><li>For example, Biologic cardiac valve prosthesis Aortic valve prosthesis</li></ul></td></tr><tr><td>Synonym</td><td><p>Synonyms are not generally added for concepts in this hierarchy.</p><ul><li><p>Exceptions: </p><ul><li>Heart in place of cardiac , such as in "biologic heart valve prosthesis" </li><li>"Bioprosthesis" for biologic cardiac valve prosthesis</li></ul></li></ul></td></tr></tbody></table>

## Modeling (stated view)

|                                                   |                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Stated parent concept(s)                          | <ul><li>14789005 |Prosthetic implant (physical object)| </li><li>303619008 |Cardiac implant (physical object)| </li><li>705991002 |Mechanical heart valve prosthesis (physical object)|, if applicable </li><li>258166002 |Custom made implant (physical object)|, if applicable</li></ul>                                                       |
| Semantic tag                                      | (physical object)                                                                                                                                                                                                                                                                                                                                |
| Attribute: Has device intended site (attribute)   | <ul><li><p>Range: &#x3C;&#x3C;123037004 |Body structure (body structure)| </p><ul><li>NOTE: While the MRCM allowed range includes the top-level concept, 123037004 |Body structure (body structure)|, only the descendants should be used in modeling cardiac valve prosthesis concepts. </li></ul></li></ul><ul><li>Cardinality: 0..1</li></ul> |
| Attribute: Has compositional material (attribute) | <ul><li><p>Range: &#x3C;&#x3C;105590001 |Substance (substance)| </p><ul><li>NOTE: While the MRCM allowed range includes the top-level concept, 105590001 |Substance (substance)|, only the descendants should be used in modeling cardiac valve prosthesis concepts. </li></ul></li></ul><ul><li>Cardinality: 0..*</li></ul>                     |
| Attribute: Is sterile (attribute)                 | <ul><li>Range: 31874001 |True (qualifier value)| OR 64100000 |False (qualifier value)</li><li>Cardinality: 0..1</li></ul>                                                                                                                                                                                                                        |

## Exemplars

The following illustrates the **stated** view for 736893007 |Aortic tri-leaflet mechanical valve prosthesis (physical object)|:

<figure><img src="../../../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/physical-object/images/174691277.png" alt=""><figcaption></figcaption></figure>

The following illustrates the **inferred** view for 736893007 |Aortic tri-leaflet mechanical valve prosthesis (physical object)|:

<figure><img src="../../../../../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/physical-object/images/174691278.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Cardiac%20Valve%20Prosthesis%20Naming%20and%20Modeling" class="button primary">Provide Feedback</a>
