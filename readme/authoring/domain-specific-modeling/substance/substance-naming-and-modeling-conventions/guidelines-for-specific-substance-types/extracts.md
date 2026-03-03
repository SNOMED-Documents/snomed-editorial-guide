# Extracts

Many extracted substances in SNOMED CT are not specific to either the part of the plant (root, seed, leaf, etc.) or the form (powder, dry or soft extract, etc.).  The specific part of the plant should be known and documented when using these substances in modeling medicinal products.  The less specific descriptions may find use in hierarchies besides Pharmaceutical / biologic product (product), such as the need to record an adverse reaction to a substance where the full details are unknown.   While the most specific information is encouraged, all levels of specificity can be represented in SNOMED CT.  &#x20;

Naming pattern:

FSN:  \[Scientific name of source organism] \<part of plant> extract (substance)

PT:  \[Common name of organism] \<part of plant> extract

SYN:  \[Scientific name of source organism] \<part of plant> extract

{% hint style="info" %}
Note:  Extraction method (via alcohol, water, CO2) is not required as it obscures the distinction between the substance and product hierarchies.  While the method of extraction is clinically important, types of solvents used in production are not required due to the need for less precise use cases.
{% endhint %}

### Extracts that include form

For extracts that include form (such as _dry_), the form should follow the source in the FSN and the corresponding SYN.  The PT can have the form either in front of or following the source, whichever is prevailing in the literature.&#x20;

* For example,&#x20;
  * FSN:  Betula dry extract (substance)
  * PT:  Dry birch extract
  * SYN:  Betula dry extract

### Naming references

Preferred references for plant scientific and common names include the following:

* Integrated Taxonomic Information System
* Catalogue of Life

Thermo Fisher Scientific may be consulted for allergens. &#x20;

The Global Substance Registration System (GSRS) is a good resource for substance names (INN, chemical names) but not necessarily the best for synonyms.&#x20;

### Level of specificity

Some requests are for extracts of which the genus is too broad, while the requirement for the species is too specific.  In these cases, the common name can be used; a scientific name is not used.&#x20;

* For example,
  * If the requested concept is for _blueberry extract_, there is no single genus and species that identifies the blueberry plant. The Vaccinium genus includes cranberry, ligonberry, and other berry plants in addition to blueberry. There are multiple blueberry species. Therefore, the concept can be created for blueberry extract without a scientific name.  The common name has a case sensitivity indicator of _ci_. &#x20;

> _See related section at_ [General Naming Conventions | Specifications SNOMED CT Editorial Guide | SNOMED International Documents](https://docs.snomed.org/snomed-ct-specifications/snomed-ct-editorial-guide/readme/authoring/general-naming-conventions#exceptions.2)

### Extract is not a type of the plant

Though an extract is derived from a substance, it is not a type of that substance.&#x20;

* For example,&#x20;
* |Ginkgo biloba extract (substance)| would not have a parent of |Ginkgo biloba (substance)|. &#x20;

<figure><img src="../../../../../../.gitbook/assets/gingko extract example.png" alt=""><figcaption></figcaption></figure>

