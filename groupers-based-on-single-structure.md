# Groupers Based on Single Structure

## Overview

Grouper concepts based on chemical structure of an active ingredient that can be sufficiently defined may be included in the |Medicinal product| hierarchy.

A high-level grouper concept supports the organization of the hierarchy based on structure: 763760008 |Medicinal product categorized by structure (product)|

## Modeling

Stated parent concept| 763158003 |Medicinal product (product)  
---|---  
Semantic tag| (product)  
Definition status| Defined  
Attribute:Has active ingredient| Range: << 105590001 |Substance (substance)|

  *     * While the allowed range is broader, the |Medicinal product| grouper concepts based on structure should only use primitive grouper concepts that are descendants of 312413002 |Substance categorized by structure (substance)| as attribute values.  

Cardinality: 0..*

  *     * While the allowed range is broader, the |Medicinal product| grouper concepts based on structure should have one and only one |Has active ingredient (attribute)|.

  
  
## Naming

**FSN**|  Product containing <active ingredient> (product)Align naming and case sensitivity with the Preferred Term for the concept that is selected as the attribute value for the 127489000 |Has active ingredient (attribute)|.For example,

  *     *       * Product containing prostaglandin (product)
      * Product containing A series prostaglandin (product)

  
---|---  
**Preferred Term**|  <Active ingredient>-containing productAlign naming and case significance with the Preferred Term for the concept that is selected as the attribute value.For example,

  *     *       * Prostaglandin-containing product
      * A series prostaglandin-containing product

  
**Synonyms**|  Synonyms matching the FSN are not required.  
  
## Exemplars

The following illustrates the **stated** view for 350067007 |Product containing prostaglandin (product)|:

<figure><img src="images/174691047.png" alt="" title=""><figcaption><p>The following illustrates the <strong>inferred</strong> view for 350067007 |Product containing prostaglandin (product)|:</p></figcaption></figure>

  

<figure><img src="images/174691046.png" alt="" title=""><figcaption><p>The following illustrates the <strong>stated</strong> view for 350068002 |Product containing A series prostaglandin (product)|:</p></figcaption></figure>

  

<figure><img src="images/174691045.png" alt="" title=""><figcaption><p>The following illustrates the <strong>inferred</strong> view for 350068002 |Product containing A series prostaglandin (product)|:</p></figcaption></figure>

  

<figure><img src="images/174691044.png" alt="" title=""></figure>

  

