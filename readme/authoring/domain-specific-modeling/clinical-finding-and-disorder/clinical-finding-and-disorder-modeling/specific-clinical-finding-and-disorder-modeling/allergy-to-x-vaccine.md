# Allergy to X vaccine

## Overview

The following modeling and terming guidelines apply to concepts in the International Release.

## Modeling

"Allergy to X vaccine" concepts shall be modeled using the proximal primitive modeling pattern. Due to the small number of concepts (n<25), no template will be created. The "Allergy to substance" template can be consulted for generalized modeling guidance.

**Single or multiple ingredient vaccine**

<table data-header-hidden><thead><tr><th width="255.8515625"></th><th>Single or multiple ingredient vaccine</th></tr></thead><tbody><tr><td>Stated parent concept</td><td>420134006 |Propensity to adverse reaction (finding)|</td></tr><tr><td>Semantic tag</td><td>(finding)</td></tr><tr><td>Definition status</td><td><p>Primitive</p><ul><li>Because 'Allergy to X vaccine' represents the propensity to an allergic reaction to any component (including excipients) of a vaccine rather than the modeled active ingredient(s), these concepts cannot be sufficiently defined. As a result, there will not be subsumption between "Allergy to X vaccine" concepts.</li></ul><ul><li>Exceptions: Grouper concept 863903001 |Allergy to component of vaccine product (finding)| is modeled as sufficiently defined and subsumes the remaining concepts.</li></ul></td></tr><tr><td>Attribute: Has realization</td><td>Attribute value = 472964009 |Allergic process (qualifier value)|</td></tr><tr><td>Attribute: Causative agent</td><td><p>Range: 787859002 |Vaccine product (medicinal product)|</p><p>Cardinality: 1..1</p><ul><li>Allergy to X vaccine concepts should have one and only one |Causative agent| attribute. </li><li>Concepts representing "vaccine product containing only" should not be used in modeling Allergy to X vaccine concepts.</li></ul></td></tr></tbody></table>

## Terming

<table data-header-hidden><thead><tr><th width="140.48443603515625"></th><th></th></tr></thead><tbody><tr><td><strong>FSN</strong></td><td><p>Use the following pattern for the FSN; align terming and case sensitivity with the FSN for the concept that represents the vaccine product that is the cause of the allergy.</p><ul><li>Allergy to component of &#x3C;Causative agent FSN> (finding)</li></ul><p>For example,</p><ul><li>Allergy to component of vaccine product containing Hepatitis A virus antigen (finding)</li><li>Allergy to component of vaccine product containing Streptococcus pneumoniae antigen (finding)</li><li>Allergy to component of vaccine product containing Clostridium tetani and Corynebacterium diphtheriae antigens (finding)</li><li>Allergy to component of vaccine product containing Measles morbillivirus and Mumps orthorubulavirus and Rubella virus antigens (finding)</li></ul></td></tr><tr><td><strong>Preferred Term</strong></td><td><p>Use the following pattern for the PT; align terming and case significance with the PT for the disorder that is the target of the vaccine. For multiple ingredient vaccine products, the disorders must be listed in alphabetical order and separated by the word "and".</p><ul><li>Allergy to &#x3C;disorder> vaccine</li><li>Allergy to &#x3C;disorder> and &#x3C;disorder> vaccine</li><li>Allergy to &#x3C;disorder> and &#x3C;disorder> and &#x3C;disorder> vaccine</li></ul><p>For example,</p><ul><li>Allergy to Hepatitis A vaccine</li><li>Allergy to pneumococcal vaccine</li><li>Allergy to diphtheria and tetanus vaccine</li><li>Allergy to measles and mumps and rubella vaccine</li></ul><p>For national extensions modeling using "vaccine containing only" product concepts, these disorder-based descriptions will need to reflect "only" to eliminate duplicate descriptions.</p></td></tr><tr><td><strong>Synonyms</strong></td><td><p>A synonym corresponding to the FSN is required.</p><p>Synonyms beginning with the disorder that is the target of the vaccine are allowed. For multiple ingredient vaccine products, the disorders must be listed in alphabetical order and separated by the word "and". Note that these are not true synonyms; they may be updated and identified as "near-synonym" descriptions when that functionality becomes available although that would also potentially require updating the PT.</p><p>For example,</p><ul><li>Hepatitis A vaccine allergy</li><li>Pneumococcal vaccine allergy</li><li>Diphtheria and tetanus vaccine allergy</li><li>Measles and mumps and rubella vaccine allergy</li></ul><p>For national extensions modeling using "vaccine containing only" product concepts, these disorder-based descriptions will need to reflect "only" to eliminate duplicate descriptions.</p></td></tr></tbody></table>

## Exemplars

The following illustrates the **stated** view for top level grouper 863903001 |Allergy to component of vaccine product (finding)|:

### Exemplars <a href="#exemplars" id="exemplars"></a>

<figure><img src="../../../../../../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **inferred** view for top level grouper 863903001 |Allergy to component of vaccine product (finding)|:

<figure><img src="../../../../../../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **stated** view for 294663006 |Allergy to component of vaccine product containing Hepatitis A virus antigen (finding)|:

<figure><img src="../../../../../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **inferred** view for  294663006 |Allergy to component of of vaccine product containing Hepatitis A virus antigen (finding)|:

<figure><img src="../../../../../../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **stated** view for 294662001 |Allergy to component of vaccine product containing Measles morbillivirus and Mumps orthorubulavirus and Rubella virus antigens (finding)|:

<figure><img src="../../../../../../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

The following illustrates the **inferred** view for 294662001 |Allergy to component of vaccine product containing Measles morbillivirus and Mumps orthorubulavirus and Rubella virus antigens (finding)|:

<figure><img src="../../../../../../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Allergy%20to%20X%20vaccine" class="button primary">Provide Feedback</a>
