# Groupers Based on Multiple Dispositions, Structures

## Overview

Groupers comprised of two or more existing disposition and/or structure groupers that can be sufficiently defined may be included in the |Medicinal product| hierarchy.

High-level grouper concepts support the organization of the combined groupers based on disposition and/or structure:

  * 766779001 |Medicinal product categorized by disposition (product)|
  * 763760008 |Medicinal product categorized by structure (product)|

## Modeling

| Stated parent concept | 763158003 \|Medicinal product (product) |
|---|---|
| Semantic tag | (product) |
| Definition status | Defined |
| Attribute: Has active ingredient | While the allowed range is broader, the \|Medicinal product\| combined grouper concepts based on disposition and/or structure should only use sufficiently defined grouper concepts that are descendants of 766739005 \|Substance categorized by disposition (substance)\| and/or primitive grouper concepts that are descendants of 312413002 \|Substance categorized by structure (substance)\| as attribute values. While the allowed range is broader, the \|Medicinal product\| combined grouper concepts should have one or more \|Has active ingredient\| attributes . Range: <<105590001 \|Substance (substance) Cardinality:0..* |

## Naming

| FSN | Product containing <Active ingredient PT> and <Active ingredient PT> (product) Product containing norepinephrine reuptake inhibitor and serotonin reuptake inhibitor (product) Product containing <Structural grouper active ingredient PT> and <Disposition grouper active ingredient PT> (product) Product containing piperazine derivative and histamine receptor antagonist (product) Use the following pattern for the FSN if the combined grouper is comprised of two dispositions or two structural groupers; align naming and case significance with the PT as described in Section 4.1 and 4.2, respectively. The active ingredients must be in alphabetical order and separated by the word “and”. For example, Use the following pattern for the FSN if the combined grouper is comprised of one disposition and one structural grouper; align naming and case significance with the FSN for the conceptwith the FSN as described in Section 4.1 and 4.2, respectively. For example, |
|---|---|
| Preferred Term | <Active ingredient PT> and <Active ingredient PT> - containing product Norepinephrine reuptake inhibitor and serotonin reuptake inhibitor-containing product <Structural grouper active ingredient PT> and <Disposition grouper active ingredient PT> - containing product Piperazine derivative and histamine receptor antagonist - containing product Use the following pattern for the PTif the combined grouper is comprised of two dispositions or two structural groupers; align naming and case significance with the PT for the concept that is selected as the attribute value.The active ingredients must be in alphabetical order and separated by the word “and". For example, Use the following pattern for the FSN if the combined grouper is comprised of one disposition and one structural grouper; align naming and case significance with the FSN for the concept that is selected as the attribute value. For example, |
| Synonyms | Synonyms matching the FSN are not required. |

## Exemplars

The following illustrates the **stated** view for combined grouper concept 767562003 |Product containing norepinephrine reuptake inhibitor and serotonin reuptake inhibitor (product)|:

<figure><img src="images/225055033.png" alt="" title=""><figcaption><p>The following illustrates the<strong>inferred</strong> view for combined grouper concept 767562003 |Product containing norepinephrine reuptake inhibitor and serotonin reuptake inhibitor (product)|:</p></figcaption></figure>

  

<figure><img src="images/225055032.png" alt="" title=""><figcaption><p>The following illustrates the <strong>stated</strong> view for combined grouper concept 70343008 |Product containing piperazine derivative and histamine receptor antagonist (product)|:</p></figcaption></figure>

  

<figure><img src="images/225055031.png" alt="" title=""><figcaption><p>The following illustrates the <strong>inferred</strong> view for combined grouper concept 70343008 |Product containing piperazine derivative and histamine receptor antagonist (product)|:</p></figcaption></figure>

  

<figure><img src="images/225055030.png" alt="" title=""></figure>

  

