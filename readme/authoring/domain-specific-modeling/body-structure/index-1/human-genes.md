# Human Genes

Human genes are modeled as cell structures in the Body structure hierarchy. Genes are named according to the _HUGO Gene Nomenclature Committee_ (HGNC).

### Naming

* FSN: \<HGNC Approved Name> gene (cell structure)
  * Note: Only add _gene_ if the HGNC Approved Name does not already include it.
  * Case sensitivity = CS
* PT: \<HGNC Gene Symbol> gene
  * Note the PT does not include a semantic tag.
  * The HGNC gene symbol is always UPPER CASE.
  * Case sensitivity = CS
* All HGNC Alias symbols must be added as additional descriptions.

#### Case Sensitivity

Conform to HGNC naming conventions. Note that HGNC approved names begin with a lowercase letter; the SNOMED FSN should retain this initial lowercase. This is an exception to SNOMED CT policy for descriptions.

### Modeling

Human genes are modeled with the following two IS A relationships:

* 382391000210108 |Gene structure (cell structure)|
  * Exception: Proto-oncogenes must be a subtype of 1396287006 |Proto-oncogene structure (cell structure)|.
* The specific Chromosomal band structure identified in the HGNC _chromosomal location_ field.
  * Structure of chromosome band _\<X>_ (cell structure)
  * If the specific band does not exist, it must be added.

#### Attribution

Each concept must include an attribution to the HGNC URI of the gene symbol report, stored in the \[Insert Specific Field/Refset Name].

&#x20;

**Example 1: COQ4**

* IS A Structure of chromosome band 9q34.11 (cell structure)
* IS A 382391000210108 |Gene structure (cell structure)|



* FSN: coenzyme Q4 gene (cell structure)
* PT: COQ4 gene
* SY: CGI-92 gene



* Attribution: HGNC: [Gene symbol report | HUGO Gene Nomenclature Committee](https://www.genenames.org/data/gene-symbol-report/#!/hgnc_id/HGNC:19693)

&#x20;

**Example 2: RET**

* IS A Structure of chromosome band 10q11.21 (cell structure)
* IS A 1396287006 |Proto-oncogene structure (cell structure)|



* FSN: ret proto-oncogene (cell structure)
* PT: RET gene
* SY: PTC gene
* SY: CDHF12 gene
* SY: RET51 gene
* SY: CDHR16 gene



* Attribution: HGNC: [Gene symbol report | HUGO Gene Nomenclature Committee](https://www.genenames.org/data/gene-symbol-report/#!/hgnc_id/HGNC:9967)

### Previous symbols and alias symbols

Previous symbols and alias symbols are added to gene concepts, followed by the word _gene_, where they are unique to a specific approved gene name. Where the same previous or alias symbols appear on multiple genes, they are to be omitted.
