# Shunt Naming and Modeling

## Naming

<table><thead><tr><th width="157.14227294921875"></th><th></th></tr></thead><tbody><tr><td>FSN</td><td><p>Use the following naming pattern for the FSN; align terming and case sensitivity with the FSN for the concepts selected as the attribute values, excluding the semantic tag.</p><p></p><p>[compositional material] [body structure] shunt (physical object)</p><p></p><ul><li><p>For example,</p><ul><li>Ventricular shunt (physical object)</li><li>Pleuroperitoneal shunt (physical object)</li></ul></li></ul></td></tr><tr><td>Preferred Term</td><td><p>Use the following naming pattern for the PT; align terming and case sensitivity with the PT for the concept that is selected as the attribute value.</p><p></p><p>[compositional material] [body structure] shunt</p><p></p><ul><li><p>For example,</p><ul><li>Ventricular shunt</li><li>Pleuroperitoneal shunt</li></ul></li></ul></td></tr><tr><td>Synonym</td><td>Synonyms are not generally added for concepts in this hierarchy.</td></tr></tbody></table>

## Modeling (stated view)

<table><thead><tr><th width="323.4271240234375"></th><th></th></tr></thead><tbody><tr><td>Stated parent concept(s)</td><td><p></p><p>257351008 |Shunt (physical object)|</p><p>Additional parent, if applicable:</p><ul><li>258166002 |Custom made implant (physical object)</li></ul></td></tr><tr><td>Semantic tag</td><td>(physical object)</td></tr><tr><td>Attribute:Has device intended site</td><td><ul><li>Note this attribute is used to model the proximal site of the shunt only. </li></ul><ul><li><p>Range: &#x3C;&#x3C;123037004 |Body structure (body structure)| </p><ul><li>NOTE: While the MRCM allowed range includes the top-level concept, 123037004 |Body structure (body structure)|, only the descendants should be used in modeling shunt concepts. </li></ul></li><li>Cardinality: 0..1</li></ul></td></tr><tr><td>Attribute: Has compositional material</td><td><ul><li><p>Range: &#x3C;&#x3C;105590001 |Substance (substance)| </p><ul><li>NOTE: While the MRCM allowed range includes the top-level concept, 105590001 |Substance (substance)|, only the descendants should be used in modeling shunt concepts. </li></ul></li><li>Cardinality: 0..*</li></ul></td></tr></tbody></table>

## Exemplars

The following illustrates the **stated** view for 258593008 |Ventricular shunt (physical object)|:

<figure><img src="../../../../../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/physical-object/images/174691266.png" alt=""><figcaption></figcaption></figure>

The following illustrates the **inferred** view for 258593008 |Ventricular shunt (physical object)|:

<figure><img src="../../../../../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Shunt%20Naming%20and%20Modeling" class="button primary">Provide Feedback</a>
