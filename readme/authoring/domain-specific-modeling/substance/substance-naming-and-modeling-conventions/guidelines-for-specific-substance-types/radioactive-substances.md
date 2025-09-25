# Radioactive substances

## Representation of radioactive isotopes

### Modeling

<table data-header-hidden><thead><tr><th width="225.53125"></th><th></th></tr></thead><tbody><tr><td><strong>Parent concept</strong></td><td><p>Most distal appropriate descendant of 89457008 |Radioactive isotope (substance)|</p><p>Most distal appropriate descendant of 33638001 |Isotope (substance)|</p></td></tr><tr><td><strong>Semantic tag</strong></td><td>(substance)</td></tr><tr><td><strong>Definition status</strong></td><td>Primitive</td></tr><tr><td><p><strong>Attribute:</strong> </p><p><strong>Is modification of</strong></p></td><td><ul><li>Range  &#x3C;105590001 |Substance (substance)|</li><li>Cardinality: 0..*</li><li>One relationship to be created to represent each modified component of the substance</li></ul></td></tr><tr><td><p><strong>Attribute:</strong> </p><p><strong>Has disposition</strong></p></td><td><ul><li><p>Range:  &#x3C;726711005 |Disposition (disposition)|</p><ul><li>NOTE: While the allowed range is broader, substance concepts should only use descendants of the concept 726711005 |Disposition (disposition)| as the attribute value.</li></ul></li><li>Cardinality: 0..1</li></ul></td></tr></tbody></table>

### Naming

Superscripts should not be used in either Fully Specified Name, Preferred Term, or synonyms.

#### FSN

Pattern:

* \[name of isotope]-\[atomic number] (substance)

For example,

* Gallium-67 (substance)

***

#### Preferred Term

Pattern:

\[name of isotope]-\[atomic number]

For example,

* Gallium-67

***

#### Synonyms

Pattern:

* \[atomic number]-\[chemical symbol]

For example,

* 67-Ga

### Exemplar

The following illustrates the hierarchy view:

<div align="left"><figure><img src="../../../../../../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure></div>

The following illustrates the **stated** and **inferred** view:

<figure><img src="../../../../../../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../../authoring/substance/images/174691609.png" alt=""><figcaption></figcaption></figure>

## Representation of radioisotope with salt

### Modeling

<table data-header-hidden><thead><tr><th width="219.58984375"></th><th></th></tr></thead><tbody><tr><td><strong>Parent concept</strong></td><td>Most distal appropriate descendant of 89457008 |Radioactive isotope (substance)|</td></tr><tr><td><strong>Semantic tag</strong></td><td>(substance)</td></tr><tr><td><strong>Definition status</strong></td><td>Primitive</td></tr><tr><td><p><strong>Attribute:</strong>  </p><p><strong>Is modification of</strong></p></td><td><ul><li>Range  &#x3C;105590001 |Substance (substance)|</li><li>Cardinality: 0..*</li><li>One relationship to be created to represent each modified component of the substance</li></ul></td></tr><tr><td><p><strong>Attribute:</strong> </p><p><strong>Has disposition</strong></p></td><td><ul><li>Range:  &#x3C;726711005 |Disposition (disposition) |</li><li>NOTE: While the allowed range is broader, substance concepts should only use &#x3C;726711005 |Disposition (disposition)| as the attribute value.</li><li>Cardinality: 0..1</li></ul></td></tr></tbody></table>

### Naming

Superscripts should not be used in either Fully Specified Name, Preferred Term, or synonyms.

Parentheses should be used to delineate the atomic number and chemical symbol from the rest of the terming; this aligns with INN.

#### FSN

Pattern:  \[name of isotope] (\[atomic number]-\[chemical symbol]) \[salt] (substance)

For example,

* Gallium (67-Ga) citrate (substance

***

#### Preferred Term

Pattern:  \[name of isotope] (\[atomic number]-\[chemical symbol]) \[salt]

For example,

* Gallium (67-Ga) citrate

### Exemplar - radioisotope with salt

The following illustrates the **stated** and **inferred** view:

<figure><img src="../../../../../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../../authoring/substance/images/174691598.png" alt=""><figcaption></figcaption></figure>

## Representation of combined radioisotope substances

## Modeling

<table data-header-hidden><thead><tr><th width="208.640625"></th><th></th></tr></thead><tbody><tr><td><strong>Parent concept</strong></td><td>Most distal appropriate descendant of 89457008 |Radioactive isotope (substance)| and a second parent identifying the labeled component</td></tr><tr><td><strong>Semantic tag</strong></td><td>(substance)</td></tr><tr><td><strong>Definition status</strong></td><td>Primitive</td></tr><tr><td><p><strong>Attribute:</strong> </p><p><strong>Is modification of</strong></p></td><td><p>Range  &#x3C;105590001 |Substance (substance)|</p><p>Cardinality: 0..*</p><p>One relationship to be created to represent each modified component of the substance</p></td></tr><tr><td><p><strong>Attribute:</strong> </p><p><strong>Has disposition</strong></p></td><td><p>Range:  &#x3C;726711005 |Disposition (disposition) |</p><ul><li>While the allowed range is broader, substance concepts should only use &#x3C;726711005 |Disposition (disposition)| as the attribute value.</li></ul><p>Cardinality: 0..1</p></td></tr></tbody></table>

### Naming

Superscripts should not be used in either Fully Specified Name, Preferred Term, or synonyms.

The Fully Specified Name should explicitly state that a component was “labeled” by a radioisotope in the FSN. Do not use “with”, “and”, or “tagged”.

Omit the word “labeled” from the PT; keep a synonym to match the FSN.

### Exemplar - combined radioisotope substances

The following illustrates both the **stated** and **inferred** view:

<figure><img src="../../../../../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../../authoring/substance/images/174691597.png" alt=""><figcaption></figcaption></figure>
