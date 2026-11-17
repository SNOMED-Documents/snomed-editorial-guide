---
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: false
  tags:
    visible: true
  actions:
    visible: true
  anchors:
    visible: false
---

# Enzyme deficiency

## Naming and modeling of enzyme deficiencies with genetic and non-genetic etiologies

Enzyme deficiencies may arise from genetic abnormalities or non-genetic mechanisms that reduce the activity or availability of an enzyme.

Where an enzyme deficiency may have either a genetic or non-genetic etiology, the naming pattern `Deficiency of <accepted enzyme name> (disorder)` shall be used for the FSN of an etiologically unspecified concept.

Where the enzyme deficiency concept specifies a gene-caused etiology, the naming pattern `<X> gene-related <Y> deficiency (disorder)` shall be used, where X represents the approved gene name in the FSN and the gene symbol in the PT. \<Y> represents the affected enzyme accepted name.

## **Modeling requirements**

Where an enzyme deficiency specifies a genetic etiology, the concept **must be modeled using the HAS ASSOCIATED GENE attribute**, with the value representing the gene responsible for the deficiency.

The **HAS ASSOCIATED GENE** relationship shall not be added to an etiologically unspecified enzyme deficiency concept solely because a genetic cause is known. The existence of genetic and non-genetic causes must be considered when determining whether the relationship is appropriate.

#### Example: Uroporphyrinogen decarboxylase deficiency

<table><thead><tr><th width="174.072998046875">Modeling component</th><th width="241.3697509765625">Etiologically unspecified concept</th><th>Genetic concept</th></tr></thead><tbody><tr><td>FSN</td><td>Deficiency of uroporphyrinogen decarboxylase (disorder)</td><td>Uroporphyrinogen decarboxylase gene-related uroporphyrinogen decarboxylase enzyme deficiency (disorder)</td></tr><tr><td>Genetic etiology</td><td>Not specified</td><td>Pathogenic variant in UROD</td></tr><tr><td>HAS ASSOCIATED GENE</td><td>Not asserted</td><td>Uroporphyrinogen decarboxylase gene (cell structure)</td></tr></tbody></table>

## Has associated gene (attribute)

HAS ASSOCIATED GENE is stated on specific genetic deficiency concepts (see decision tree below), and on genetic diseases only when the disease mechanism is not a deficiency. Diseases caused by a deficiency are modeled with DUE TO = the deficiency concept and never carry the gene.

1. **Genetic Deficiency concepts** state HAS DEFICIENCY OF the deficient gene product (protein or RNA). Add the substance where needed to define the deficiency.&#x20;
2. **Diseases caused by a deficiency** use DUE TO = the deficiency concept, not IS A the deficiency.  IS A parents follow the phenotype under the normal rules. Never state HAS ASSOCIATED GENE on these diseases.
3. **Criteria for adding a gene relationship to a Deficiency of X concept.** State the HAS ASSOCIATED GENE relationship on every concept that meets all of the following:

* variants in the gene are disease-causing and present in every instance of the concept;
* it is the causal gene, which may differ from the gene encoding the deficient product (for example SUMF1 in multiple sulfatase deficiency);
* it is supported by a cited source (Orphanet, OMIM, GeneReviews or a recent review).
* when the gene is named in the FSN, and is one of multiple etiologies for the deficiency.

4. **Multiple values mean all of them.** Multiple HAS ASSOCIATED GENE, HAS DEFICIENCY OF or DUE TO values assert that **all apply** to every instance. Use separate subtypes to represent differing etiologies.

### Genetic Deficiency concepts

![](<../../../../../../.gitbook/assets/Pasted image 2026-11-17 20.06.56.png>)

Inherited and acquired forms sit beside these branches:

* **Genetic and acquired forms**: add Inherited deficiency of X or Acquired deficiency of X only when a disease needs one as its DUE TO value. If one gene causes the inherited form, the gene goes on the Inherited deficiency of X concept.

#### Combined deficiency

A combined deficiency is one disorder in which two or more gene products are deficient together. _Combined_ describes the products, not the genetics. State one HAS DEFICIENCY OF per deficient product; where the gene goes depends on how the combination arises.

| How the combination arises                                                          | Example                                                          | Concepts and gene                                                                                                                  |
| ----------------------------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| One gene causes deficiency of several products                                      | Multiple sulfatase deficiency (SUMF1)                            | One concept: HAS DEFICIENCY OF each product + HAS ASSOCIATED GENE SUMF1; no gene name in the FSN                                   |
| Any one of several genes causes the same combination; each gene alone is sufficient | Combined deficiency of factor V and factor VIII (LMAN1 or MCFD2) | Generic combined deficiency with no gene; one “\[gene] gene-related combined deficiency of …” subtype per gene, each with its gene |
| Variants in more than one gene are required together (digenic)                      | None identified yet                                              | One concept with every required gene stated, since all apply to every instance                                                     |

Not combined deficiencies:

* **Deficiency of one multi-subunit product** encoded by several genes (for example, a respiratory chain complex): one deficient product, so model it as a single deficiency with gene-related subtypes.
* **Separate deficiencies that happen to co-occur** in a patient:  record each deficiency separately.

### Naming conventions

The gene appears in an FSN only when it distinguishes the concept from a parent that has other causes. Otherwise the gene is carried in the definition and a synonym, when requested.

<table data-search="false"><thead><tr><th>Concept</th><th>FSN pattern</th><th>Gene in FSN?</th></tr></thead><tbody><tr><td>Deficiency, single-gene or any cause</td><td>Deficiency of [product] (disorder)</td><td>No; “[gene] gene-related deficiency of [product]” may be a synonym when single-gene</td></tr><tr><td>Gene-specific subtype of a deficiency with other causes</td><td>[gene] gene-related deficiency of [product] (disorder)</td><td>Yes</td></tr><tr><td>Inherited or acquired subtype</td><td>Inherited deficiency of [product] (disorder); Acquired deficiency of [product] (disorder)</td><td>No</td></tr><tr><td>Combined deficiency</td><td>Combined deficiency of [product A] and [product B] (disorder)</td><td>No</td></tr><tr><td>Gene-specific subtype of a combined deficiency</td><td>[gene] gene-related combined deficiency of [product A] and [product B] (disorder)</td><td>Yes</td></tr><tr><td>Disease due to a deficiency</td><td>[disease] due to deficiency of [product] (disorder), or due to [gene] gene-related deficiency of [product]</td><td>Only through the named deficiency</td></tr><tr><td>Gene-specific subtype of a non-deficiency disease</td><td>[gene] gene-related [disease] (disorder)</td><td>Yes</td></tr></tbody></table>

* **Product name:** use the name of the substance concept that is the HAS DEFICIENCY OF value, spelled out (for example, _transfer ribonucleic acid_, not _tRNA_). Abbreviations go in synonyms.
* **Gene name**: the FSN uses the gene concept’s full name; the preferred term uses the HGNC symbol (for example, _MT-TK gene-related deficiency of mitochondrial tRNA(Lys)_).
* **Established disease names**: Where a named syndrome exists, it keeps its recognized name as the FSN; the _due to deficiency of_ wording can be a synonym.

![Resulting disease · 3 questions, 4 outcomes](<../../../../../../.gitbook/assets/resulting disease · 3 questions, 4 outcomes.png>)

The DUE TO value must match the disease’s scope exactly. A disease requiring deficiency of both X and Y uses multiple DUE TO relationships.

| The disease can arise from              | DUE TO value                                     |
| --------------------------------------- | ------------------------------------------------ |
| any form of deficiency of X             | Deficiency of X                                  |
| Deficiency of X, more than one gene     | Specific subtype for each deficiency of X        |
| Deficiency of X, one gene               | the concept carrying that gene (Deficiency of X) |
| one gene only, where other causes exist | \<gene>-related deficiency of X                  |
| Multiple deficiencies required          | Multiple DUE TO relationships for X and Y        |

### Retrieval note for implementers

Genes on deficiency-mediated diseases are reached through DUE TO, so finding every disorder associated with a gene needs both clauses:

> (< 64572001 |Disease| : 1395996007 |Has associated gene (attribute)| = < 382391000210108 |Gene structure (cell structure)|)
>
> OR\
> (< 64572001 |Disease| : 42752001 |Due to| = (\* : 1395996007 |Has associated gene (attribute)| = < 382391000210108 |Gene structure (cell structure)|))
>
> <br>



\
<br>
