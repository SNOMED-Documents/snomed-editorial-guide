# Stent Naming and Modeling

## Naming

<table data-header-hidden><thead><tr><th width="105.7513427734375"></th><th></th></tr></thead><tbody><tr><td>FSN</td><td><p>Use the following naming pattern for the FSN; align terming and case sensitivity with the FSN for the concepts selected as the attribute values, excluding the semantic tag.</p><p></p><p>[Is sterile] [absorbability] [compositional material] [coating] [device intended site] stent (physical object)</p><p></p><ul><li><p>For example,</p><ul><li>Custom-made bioabsorbable vaginal stent (physical object)</li><li>Bare metal renal artery stent (physical object)</li><li>Silicon carbide coated intracranial vascular stent (physical object)</li><li>Sterile polymer coated metal esophageal stent (physical object)</li></ul></li></ul></td></tr><tr><td>Preferred Term</td><td><p>Use the following naming pattern for the PT; align terming and case sensitivity with the PT for the concept that is selected as the attribute value.  For multiple ingredient drug products, the active ingredients must be in alphabetical order and separated by the word “and”.</p><p></p><p>[Is sterile] [absorbability] [compositional material] [coating] [device intended site] stent</p><ul><li><p>For example,</p><ul><li>Custom-made bioabsorbable vaginal stent</li><li>Bare metal renal artery stent</li><li>Silicon carbide coated intracranial vascular stent</li><li>Sterile polymer coated metal esophageal stent</li></ul></li></ul></td></tr><tr><td>Synonym</td><td>Synonyms are not generally added for concepts in this hierarchy.</td></tr></tbody></table>

## Modeling

<table data-header-hidden><thead><tr><th width="304.1302490234375"></th><th></th></tr></thead><tbody><tr><td>Stated parent concept</td><td><p>65818007 |Stent (physical object)|</p><p></p><p>258166002 |Custom made implant (physical object)|, if applicable</p><p></p><ul><li>Exception: 411114003 |Drug coated stent (product)| is modeled with an additional stated parent of 411115002 |Drug-device combination product (product)| </li></ul></td></tr><tr><td>Semantic tag</td><td>(physical object)</td></tr><tr><td>Attribute: Has absorbability</td><td><ul><li>Range: 860574003 |Bioabsorbable (qualifier value)| OR 863965006 |Nonbioabsorbable (qualifier value)| OR 863968008 |Partially bioabsorbable (qualifier value)| </li><li>Cardinality: 0..1</li></ul></td></tr><tr><td>Attribute: Has coating material</td><td><ul><li>Range: &#x3C; 105590001 |Substance (substance)| </li><li>Cardinality: 0..1</li></ul></td></tr><tr><td>Attribute: Has compositional material</td><td><ul><li><p>Range: &#x3C;&#x3C;105590001 |Substance (substance)| </p><ul><li>NOTE: While the MRCM allowed range includes the top-level concept, 105590001 |Substance (substance)|, only the descendants should be used in modeling stent concepts.</li></ul></li><li>Cardinality: 0..*</li></ul></td></tr><tr><td>Attribute: Has device intended site</td><td><ul><li><p>Range: &#x3C;&#x3C;123037004 |Body structure (body structure)| </p><ul><li>NOTE: While the MRCM allowed range includes the top-level concept, 123037004 |Body structure (body structure)|, only the descendants should be used in modeling stent concepts. </li></ul></li><li>Cardinality: 0..1</li></ul></td></tr><tr><td>Attribute: Is sterile</td><td><ul><li>Range: 31874001 |True (qualifier value)| OR 64100000 |False (qualifier value) </li></ul><ul><li>Cardinality: 0..1</li></ul></td></tr></tbody></table>

## Exemplars

The following illustrates the **stated** view for 716668000 |Non-sterile bare metal esophageal stent (physical object)|:

<figure><img src="../../../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/physical-object/images/174691271.png" alt=""><figcaption></figcaption></figure>

The following illustrates the **inferred** view for 716668000 |Non-sterile bare metal esophageal stent (physical object)|:

<figure><img src="../../../../../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Stent%20Naming%20and%20Modeling" class="button primary">Provide Feedback</a>
