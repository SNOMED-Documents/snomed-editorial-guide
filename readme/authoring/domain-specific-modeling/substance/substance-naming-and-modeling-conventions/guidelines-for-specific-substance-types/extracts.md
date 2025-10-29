# Extracts

Many extracted substances in SNOMED CT are not specific to either the part of the plant (root, seed, leaf, etc.) or the form (powder, dry or soft extract, etc.).  The specific part of the plant should be known and documented when using these substances in modeling medicinal products.  The less specific descriptions may find use in hierarchies besides Pharmaceutical / biologic product (product), such as the need to record an adverse reaction to a substance where the full details are unknown.   While the most specific information is encouraged, all levels of specificity can be represented in SNOMED CT.  &#x20;

Naming pattern:

FSN:  \[Scientific name of source organism] \<part of plant> \<form> extract (substance)

PT:  \[Common name of organism] \<part of plant> extract\*

SYN:  \[Scientific name of source organism] \<part of plant> \<form> extract

{% hint style="info" %}
Note:  Extraction method (via alcohol, water, CO2) is not required as it obscures the distinction between the substance and product hierarchies.  While the method of extraction is clinically important, types of solvents used in production are not required due to the need for less precise use cases.
{% endhint %}

\*For extracts that include form, the form should follow the source in the FSN and the corresponding SYN.  The PT can have the form either in front of or following the source, whichever is prevailing in the literature.&#x20;

* For example,&#x20;
  * FSN:  Betula dry extract (substance)
  * PT:  Dry birch extract
  * SYN:  Betula dry extract

\
