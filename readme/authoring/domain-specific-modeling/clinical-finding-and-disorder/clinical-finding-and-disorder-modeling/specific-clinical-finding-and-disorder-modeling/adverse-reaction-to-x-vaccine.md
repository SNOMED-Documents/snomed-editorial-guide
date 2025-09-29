# Adverse reaction to X vaccine

## Overview

The following modeling and terming guidelines apply to concepts in the International Release.

## Modeling

"Adverse reaction to X vaccine" concepts shall be modeled using the proximal primitive modeling pattern. Due to the small number of concepts (n<50), no template will be created. The "Adverse reaction to substance" template can be consulted for generalized modeling guidance.

**Single or multiple ingredient vaccine**

<table data-header-hidden><thead><tr><th width="250.98046875">Feature</th><th></th></tr></thead><tbody><tr><td><strong>Stated parent concept</strong></td><td>281647001 |Adverse reaction (disorder)|</td></tr><tr><td><strong>Semantic tag</strong></td><td>(disorder)</td></tr><tr><td><strong>Definition status</strong></td><td><p>Primitive</p><ul><li><strong>Note</strong>: Because 'Adverse reaction to X vaccine' represents the propensity to an adverse reaction to any component (including excipients) of a vaccine rather than the modeled active ingredient(s), these concepts cannot be sufficiently defined. As a result, there will not be subsumption between "Adverse reaction to X vaccine" concepts.</li><li><strong>Exceptions</strong>: Grouper concepts 293104008 |Adverse reaction to component of vaccine product (disorder)|, 219075006 |Adverse reaction to component of vaccine product containing bacteria antigen (disorder)|, and 408672009 |Adverse reaction to component of vaccine product containing virus antigen (disorder)| are modeled as sufficiently defined and subsume the remaining concepts.</li></ul></td></tr><tr><td><p><strong>Attribute:</strong></p><p><strong>Causative agent</strong></p></td><td><ul><li>Range: &#x3C;&#x3C;787859002 |Vaccine product (medicinal product)|</li><li><p>Cardinality: 1..1</p><ul><li>Adverse reaction to X vaccine concepts should have one and only one |Causative agent| attribute.</li><li>Concepts representing "vaccine product containing only" should not be used in modeling Adverse reaction to X vaccine concepts.</li></ul></li></ul></td></tr></tbody></table>

## Terming

<table data-header-hidden><thead><tr><th width="142.3636474609375"></th><th></th></tr></thead><tbody><tr><td><strong>FSN</strong></td><td><p>Use the following pattern for the FSN; align terming and case sensitivity with the FSN for the concept that represents the vaccine product that is the cause of the adverse reaction.</p><ul><li>Adverse reaction to component of &#x3C;Causative agent FSN> (disorder)</li></ul><p>For example,</p><ul><li>Adverse reaction to component of vaccine product containing Hepatitis A virus antigen (disorder)</li><li>Adverse reaction to component of vaccine product containing Streptococcus pneumoniae antigen (disorder)</li><li>Adverse reaction to component of vaccine product containing only Clostridium tetani and Corynebacterium diphtheriae antigens (disorder)</li><li>Adverse reaction to component of vaccine product containing Measles morbillivirus and Mumps orthorubulavirus and Rubella virus antigens (disorder)</li></ul></td></tr><tr><td><strong>Preferred Term</strong></td><td><p>Use the following pattern for the PT; align terming and case significance with the PT for the disorder that is the target of the vaccine. For multiple ingredient vaccine products, the disorders must be listed in alphabetical order and separated by the word "and".</p><ul><li>Adverse reaction to &#x3C;disorder> vaccine</li><li>Adverse reaction to &#x3C;disorder> and &#x3C;disorder> vaccine</li><li>Adverse reaction to &#x3C;disorder> and &#x3C;disorder> and &#x3C;disorder> vaccine</li></ul><p>For example,</p><ul><li>Adverse reaction to hepatitis A vaccine</li><li>Adverse reaction to pneumococcal vaccine</li><li>Adverse reaction to diphtheria and tetanus vaccine</li><li>Adverse reaction to measles and mumps and rubella vaccine</li></ul><p>For national extensions modeling using "vaccine containing only" product concepts, these disorder-based descriptions will need to reflect "only" to eliminate duplicate descriptions.</p></td></tr><tr><td><strong>Synonyms</strong></td><td><p>A synonym corresponding to the FSN is required.</p><p>Synonyms beginning with the disorder that is the target of the vaccine are allowed. For multiple ingredient vaccine products, the disorders must be listed in alphabetical order and separated by the word "and". Note that these are not true synonyms; they may be updated and identified as "near-synonym" descriptions when that functionality becomes available although that would also potentially require updating the PT.</p><p>For example,</p><ul><li>Hepatitis A vaccine adverse reaction</li><li>Pneumococcal vaccine adverse reaction</li><li>Diphtheria and tetanus vaccine adverse reaction</li><li>Measles and mumps and rubella vaccine adverse reaction</li></ul><p>For national extensions modeling using "vaccine containing only" product concepts, these disorder-based descriptions will need to reflect "only" to eliminate duplicate descriptions.</p></td></tr></tbody></table>

## Exemplars

The following illustrates the **stated** and **inferred** view for top level grouper 293104008 |Adverse reaction to vaccine product (disorder)|:

<figure><img src="../../../../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="blob:https://conf.spaces.snomed.org/d39d6c6f-0808-441e-b4ee-20a147e262f9#media-blob-url=true&#x26;id=c686d6f2-19d1-4dca-b5fa-caa4b4b3ea02&#x26;collection=contentId-133240726&#x26;contextId=133240726&#x26;mimeType=application%2Foctet-stream&#x26;name=Screen%20Shot%202020-07-13%20at%2010.42.35%20AM.png&#x26;size=30032&#x26;width=765&#x26;height=183&#x26;alt=" alt=""><figcaption></figcaption></figure>

The following illustrates the **stated** view for top level grouper 219075006 |Adverse reaction to vaccine product containing bacteria antigen (disorder)|:

<figure><img src="../../../../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **inferred** view for top level grouper 219075006 |Adverse reaction to vaccine product containing bacteria antigen (disorder)|:

<figure><img src="../../../../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **stated** view for single ingredient vaccine 293126009 |Adverse reaction to vaccine product containing Hepatitis A virus antigen (disorder)|:

<figure><img src="../../../../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **inferred** view for single ingredient vaccine 293126009 |Adverse reaction to vaccine product containing Hepatitis A virus antigen (disorder)|:

<figure><img src="../../../../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **stated** view for multiple ingredient vaccine 293125008 |Adverse reaction to vaccine product containing Measles morbillivirus and Mumps orthorubulavirus and Rubella virus antigens (disorder)|:

<figure><img src="../../../../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **inferred** view for multiple ingredient vaccine 293125008 |Adverse reaction to vaccine product containing Measles morbillivirus and Mumps orthorubulavirus and Rubella virus antigens (disorder)|:

<figure><img src="../../../../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../../authoring/clinical-finding-and-disorder/images/174690451.png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Adverse%20reaction%20to%20X%20vaccine" class="button primary">Provide Feedback</a>
