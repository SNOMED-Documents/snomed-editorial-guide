# Supporting hierarchy - Disposition

## Overview

The hierarchy, 726711005 |Disposition (disposition)|, was created to support the remodeling of the Substance hierarchy. The concepts in this hierarchy are used as the attribute value for the |Has disposition (attribute)| for concepts in the Substance hierarchy, to sufficiently define grouper concepts representing dispositions, and to sufficiently define concepts in other SNOMED CT hierarchies. To provide adequate context to differentiate concepts in this hierarchy from similar concepts in other existing SNOMED CT hierarchies, a new (disposition) semantic tag was created.

## Modeling

<table data-header-hidden><thead><tr><th width="224.31640625"></th><th></th></tr></thead><tbody><tr><td><strong>Parent concept</strong></td><td>&#x3C;&#x3C;726711005 |Disposition (disposition)|</td></tr><tr><td><strong>Semantic tag</strong></td><td>(disposition)</td></tr><tr><td><strong>Definition status</strong></td><td>Primitive</td></tr><tr><td><strong>Attributes</strong></td><td>Not applicable</td></tr></tbody></table>

## Terming Guidelines

### General Terming Guidelines

The following words should be avoided unless specifically identified as an exception in the editorial guidelines.

* agent
* analog
* and
* and/or
* content(s)
* derivative
* material
* metabolite
* modification
* or
* preparation
* product
* substance

Exceptions:

* Alkylating agent (disposition)
* Chelating agent (disposition)

{% hint style="warning" %}
Descriptions should be singular, not plural.
{% endhint %}

### **Disposition representing: receptor agonist, receptor antagonist, enzyme inhibitor, enzyme activator**

* **receptor agonist or partial agonist**
* **receptor antagonist or partial antagonist**
* **enzyme inhibitor or**\
  **enzyme system inhibitor**
* **enzyme activator**

#### FSN

Patterns:

* _**X**_ receptor agonist (disposition)
* _**X**_ receptor antagonist (disposition)
* _**X**_ inhibitor (disposition)
* _**X**_ activator (disposition)

Example of receptor agonist:

* Dopamine receptor agonist (disposition)
* Opioid receptor agonist (disposition)
* Opioid receptor partial agonist (disposition)

Example of receptor antagonist:

* Beta-adrenergic receptor antagonist (disposition)
* Histamine receptor antagonist (disposition)
* Opioid receptor antagonist (disposition)
* Opioid receptor partial antagonist (disposition)

Example of inhibitor (enzyme):

* Acetylcholinesterase inhibitor (disposition)
* Phosphodiesterase 5 inhibitor (disposition)

Example of inhibitor (enzyme system):

* Hydrogen/potassium adenosine triphosphatase enzyme system inhibitor (disposition)
* Selective serotonin reuptake inhibitor (disposition)

Example of activator:

* Plasminogen activator (disposition)

#### Preferred Term

Patterns:

* _**X**_ receptor agonist
* _**X**_ receptor antagonist
* _**X**_ inhibitor
* _**X**_ activator

Example of receptor agonist:

* Dopamine receptor agonist
* Opioid receptor agonist

Example of receptor antagonist:

* Beta-adrenergic receptor antagonist
* Histamine receptor antagonist
* Opioid receptor antagonist

Example of enzyme inhibitor:

* Acetylcholinesterase inhibitor
* Phosphodiesterase 5 inhibitor
* Centrally acting acetylcholinesterase inhibitor

Example of enzyme system inhibitor:

* Proton pump inhibitor
* Selective serotonin reuptake inhibitor

Example of enzyme inducer:

* Plasminogen activator

Exceptions:

* Preferred terms may reflect the common clinical description for a disposition.
  * Example:
    * |Hydrogen/potassium adenosine triphosphatase enzyme system inhibitor (disposition)| has Preferred Term |Proton pump inhibitor|
    * |3-Hydroxy-3-methylglutaryl-coenzyme A reductase inhibitor (disposition)| has Preferred Term |HMG-CoA reductase inhibitor|

#### Synonyms

Synonyms are not allowed unless explicitly identified as an exception.

### **Disposition representing: Response induced in an organism by a substance**

#### FSN

Pattern:

* _**X**_ (disposition)

Example:

* Growth factor (disposition)
* Cytokine (disposition)
* Carcinogen (disposition)
* Potassium channel blocker (disposition)
* Calcium channel blocker (disposition)
* Fusion inhibitor (disposition)

#### Preferred Term

Pattern:

* _**X**_

Example:

* Growth factor
* Cytokine
* Carcinogen
* Potassium channel blocker
* Calcium channel blocker
* Fusion inhibitor

#### Synonyms

Synonyms are not allowed unless explicitly identified as an exception.

### **Disposition representing - a chemical effect or physical property**

#### FSN

Pattern:

* _**X**_ (disposition)

Example:

* Alkylating agent (disposition)
* Chelating agent (disposition)

#### Preferred Term

Pattern:

* _**X**_

Example:

* Alkylating agent
* Chelating agent

#### Synonyms

Synonyms are not allowed unless explicitly identified as an exception.

## Exemplar

The following illustrates the **stated** and **inferred** view:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (162).png" alt="" width="563"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (163).png" alt="" width="530"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (164).png" alt="" width="563"><figcaption></figcaption></figure></div>

<figure><img src="../../../../authoring/substance/images/174691643.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../authoring/substance/images/174691644.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../authoring/substance/images/174691645.png" alt=""><figcaption></figcaption></figure>
