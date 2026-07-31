# Human Genes

Human genes are represented as cell structures (subcellular structures) within the Body structure hierarchy. This reflects the biological reality of genes as physical, organized, functional units within chromosomes.

This approach is consistent with the Foundational Model of Anatomy, the Sequence Ontology, and the _HUGO Gene Nomenclature Committee's_ (HGNC) defining characteristic of chromosomal location. It enables participation of gene concepts in the full SNOMED CT concept model, including hierarchical classification, relationship-based definitions, and use with existing attributes such as FINDING SITE and INHERES IN.&#x20;

Genes are named according to the _HUGO Gene Nomenclature Committee_ (HGNC).

### Naming

* FSN:  \<HGNC Approved Name> gene (cell structure)
  * Only add _gene_ if the HGNC Approved Name does not already include it
  * Case sensitivity = CS
* PT:  \<HGNC Gene Symbol> gene
  * The HGNC gene symbol is always UPPER CASE (alias and previous symbols may contain lower case letters)
  * Case sensitivity = CS
* All HGNC Alias symbols must be added as additional descriptions.

#### Case Sensitivity

The case sensitivity for approved gene names must conform to HGNC naming conventions. Approved names and symbols may be found at [https://www.genenames.org/](https://www.genenames.org/). Note that most HGNC approved names begin with a lowercase letter; the SNOMED FSN should retain this initial lowercase. This is an exception to SNOMED CT policy for descriptions and will generate a warning in the Authoring platform.

### Modeling

Human genes are modeled with the following two IS A relationships:

* 382391000210108 |Gene structure (cell structure)|
  * Exception: Proto-oncogenes must be a subtype of 1396287006 |Proto-oncogene structure (cell structure)|
* The specific Chromosomal band structure identified in the HGNC _chromosomal location_ field
  * Structure of chromosome band _\<X>_ (cell structure)
  * If the specific band does not exist, it must be created.

#### Attribution

Each concept must include an attribution to the HGNC URI of the gene symbol report, stored as an attribution annotation.

&#x20;

**Example 1:** Elastin gene

![](<../../../../../.gitbook/assets/unknown (3).png>)

&#x20;

**Example 2:** Apolipoprotein B gene

![](<../../../../../.gitbook/assets/unknown (4).png>)

### Previous symbols and alias symbols

Previous symbols and alias symbols are added to gene concepts, followed by the word _gene_, where they are unique to a specific approved gene name. Where the same previous or alias symbols appear on multiple genes, they are to be omitted.
