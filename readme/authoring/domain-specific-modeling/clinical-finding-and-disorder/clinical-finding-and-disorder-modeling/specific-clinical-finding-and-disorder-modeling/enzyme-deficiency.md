# Enzyme deficiency

## Naming and modeling of enzyme deficiencies with genetic and non-genetic etiologies

Enzyme deficiencies may arise from genetic abnormalities or non-genetic mechanisms that reduce the activity or availability of an enzyme.

Where an enzyme deficiency may have either a genetic or non-genetic etiology, the naming pattern `Deficiency of <accepted enzyme name> (disorder)` shall be used for the FSN of an etiologically unspecified concept.

Where the enzyme deficiency concept specifies a gene-caused etiology, the naming pattern `<X> gene-related <Y> deficiency (disorder)` shall be used, where X represents the approved gene name in the FSN and the gene symbol in the PT.  \<Y> represents the affected enzyme accepted name.

### **Modeling requirements**

Where an enzyme deficiency specifies a genetic etiology, the concept **must be modeled using the HAS ASSOCIATED GENE attribute**, with the value representing the gene responsible for the deficiency.

The **HAS ASSOCIATED GENE** relationship shall not be added to an etiologically unspecified enzyme deficiency concept solely because a genetic cause is known. The existence of genetic and non-genetic causes must be considered when determining whether the relationship is appropriate.

#### Example:  Uroporphyrinogen decarboxylase deficiency

<table><thead><tr><th width="174.072998046875">Modeling component</th><th width="241.3697509765625">Etiologically unspecified concept</th><th>Genetic concept</th></tr></thead><tbody><tr><td>FSN</td><td>Deficiency of uroporphyrinogen decarboxylase (disorder)</td><td>Uroporphyrinogen decarboxylase gene-related uroporphyrinogen decarboxylase enzyme deficiency (disorder)</td></tr><tr><td>Genetic etiology</td><td>Not specified</td><td>Pathogenic variant in UROD</td></tr><tr><td>HAS ASSOCIATED GENE</td><td>Not asserted</td><td>Uroporphyrinogen decarboxylase gene (cell structure)</td></tr></tbody></table>

<br>
