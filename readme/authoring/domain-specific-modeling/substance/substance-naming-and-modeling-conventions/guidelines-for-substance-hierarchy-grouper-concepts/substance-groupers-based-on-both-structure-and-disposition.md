# Substance Groupers Based on Both Structure and Disposition

## Overview

Groupers based on both structure and disposition that are deemed to be clinically useful and that can be sufficiently defined will be included in the |Substance| hierarchy.

_Note: This section applies to concepts representing a single structural parent and a single disposition. It does not apply concepts representing more than one structural parent or disposition._

## Modeling

<table data-header-hidden><thead><tr><th width="222.640625">Stated parent concept</th><th>The stated parent concept must be the concept that represents the structural grouper. If such a concept does not exist, it must be created and its stated substance descendants added before the grouper based on both structure and disposition can be created.</th></tr></thead><tbody><tr><td><strong>Stated parent concept</strong></td><td>The stated parent concept must be the concept that represents the structural grouper. If such a concept does not exist, it must be created and its stated substance descendants added before the grouper based on both structure and disposition can be created.</td></tr><tr><td><strong>Definition status</strong></td><td>Defined</td></tr><tr><td><p><strong>Attribute:</strong></p><p><strong>Has disposition</strong></p></td><td><p>Range: &#x3C;726711005 |Disposition (disposition)|</p><ul><li>While the allowed range is broader, the Substance Groupers based on both Structure and Disposition should only use &#x3C;726711005 |Disposition (disposition) as the attribute value.</li></ul><p>Cardinality: 1..1</p></td></tr></tbody></table>

## Exemplar for Grouper Concept Based on both Structure and Disposition

The following illustrates the **stated** and **inferred** view for grouper concepts based on both structure and disposition.

<figure><img src="../../../../../../.gitbook/assets/image (111).png" alt=""><figcaption><p>Figure:  Stated view of 438942000 |Piperidine derivative with histamine receptor antagonist mechanism of action (substance)|</p></figcaption></figure>

<figure><img src="../../../../../../.gitbook/assets/image (112).png" alt=""><figcaption><p>Figure:  Inferred view of 438942000 |Piperidine derivative with histamine receptor antagonist mechanism of action (substance)|</p></figcaption></figure>

## Terming

### FSN

Use the following pattern for the FSN, with X representing the structure and Y representing the disposition. The FSN should align with the FSN for the substance grouper and disposition used as the stated parent and attribute value respectively.

* X with Y mechanism of action (substance)

For example,

* Piperazine derivative with histamine H1 receptor antagonist mechanism of action (substance)
* Substance with dihydropyridine derivative structure and calcium channel blocker mechanism of action (substance)
* Substance with organophosphorus structure and acetylcholinesterase inhibitor mechanism of action (substance)

***

### Preferred Term

Use the following pattern for the Preferred Term, with X representing the structure and Y representing the disposition. The FSN should align with the FSN for the substance grouper and disposition used as the stated parent and attribute value respectively.

* X Y

For example,

* Piperazine derivative histamine H1 receptor antagonist
* Dihydropyridine derivative calcium channel blocker
* Organophosphorus acetylcholinesterase inhibitor

***

### Synonyms

A synonym to match the FSN is not required.

Additional synonyms are allowed only if they are consistent with the synonyms for the corresponding structure grouper and disposition.

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Substance%20Groupers%20Based%20on%20Both%20Structure%20and%20Disposition" class="button primary">Provide Feedback</a>
