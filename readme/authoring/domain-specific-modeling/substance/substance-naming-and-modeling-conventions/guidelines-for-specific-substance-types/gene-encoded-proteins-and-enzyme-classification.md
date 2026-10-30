# Gene-encoded proteins and enzyme classification

## Scope

This guidance applies to specific protein products encoded by individual genes and defines how these concepts shall be modeled in relation to enzyme classification concepts within the substance hierarchy under 90668006 |Substance with enzyme mechanism of action (substance)|.

A gene-encoded protein and the Enzyme Commission (EC) enzyme class associated with its catalytic activity represent distinct concepts at different levels of biological specificity.

* Enzyme class: For example, 1-acylglycerol-3-phosphate O-acyltransferase (EC 2.3.1.51) represents a functional category comprising enzymes that catalyse a defined biochemical reaction, irrespective of their protein structure or gene of origin.
* Gene-encoded protein: For example, 1-acyl-sn-glycerol-3-phosphate acyltransferase beta represents the AGPAT2 protein, a specific protein product identified by its encoding gene and protein structure. It is associated with the enzymatic activity represented by the corresponding EC class but is not defined solely by that activity.

Distinct proteins encoded by different genes may share the same EC classification because different gene products can catalyse the same biochemical reaction.

EC-class disposition groupers therefore remain necessary even when specific protein subtypes have been created. They support modeling use cases in which the gene source of an enzymatic activity is unknown or clinically irrelevant. For example, in disorder modeling, the relevant level of specificity may be the causative enzyme class rather than the specific protein.

## Modeling principle

A specific gene-encoded protein associated with an enzymatic activity shall be modelled as a subtype (IS A) of both:

* 88878007 |Protein (substance)|; and
* the corresponding leaf-level EC enzyme class substance concept.

The second IS A relationship represents the functional association between the protein and the enzyme class: the protein has the enzymatic activity defined by that EC class. The protein concept itself remains identified by its gene source and protein structure.

**Stated vs inferred IS A**: The IS A 88878007 |Protein (substance)| relationship is stated. The IS A to the corresponding EC leaf-class concept is inferred by the classifier through the Has disposition relationship and shall not be stated explicitly.

Creating a specific protein subtype shall not modify or replace the corresponding EC class concept. The EC class and the gene-encoded protein represent distinct modelling purposes and shall coexist within the hierarchy.

**Multifunctional proteins**: A protein with more than one independent catalytic activity shall be modelled with multiple Has disposition values, one for each EC activity, each linked to a distinct EC leaf-level concept.

**Enzyme subunits and non-catalytic gene products**: Gene products that form part of an enzyme complex but lack independent catalytic activity (such as regulatory or structural subunits) shall not carry a Has disposition value and shall not be inferred as subtypes of an EC leaf-class concept. These are modelled as subtypes of 88878007 |Protein (substance)| only.

**Isoforms**: One concept shall be created per UniProt canonical entry. A separate concept for an isoform shall be created only when the isoform has its own established name (not merely "isoform 1", "isoform 2"), has a different EC number or distinct catalytic activity, and there is a documented clinical reason to distinguish it. Where isoforms share the same function, they are covered by the canonical concept, with established isoform names added as acceptable synonyms. Where a functionally distinct isoform does warrant its own concept, it shall be modelled as a sibling of the canonical protein concept — IS A 88878007 |Protein (substance)| and Has disposition → the corresponding EC activity — not as a subtype of the canonical protein.

The following example illustrates the relationship between an EC enzyme class and a specific gene-encoded protein.

* **EC enzyme class:** 45952002 |Substance with 1-acylglycerol-3-phosphate O-acyltransferase mechanism of action (substance)| represents the EC 2.3.1.51 enzyme class and is modelled with Has disposition = 1418060000 |1-acylglycerol-3-phosphate O-acyltransferase (disposition)|.
* **Gene-encoded protein**: 1417977000 |1-acyl-sn-glycerol-3-phosphate acyltransferase beta (substance)| represents the AGPAT2 protein, encoded by the AGPAT2 gene, which catalyses the corresponding reaction. It is modelled as a subtype of 45952002 |Substance with 1-acylglycerol-3-phosphate O-acyltransferase mechanism of action (substance)|.

This modeling approach preserves the distinction between the functional classification of an enzyme and the identity of a specific protein product.

## Naming conventions for gene-encoded protein concepts

**FSN and PT**: Use the UniProt-recommended protein name for both the FSN and PT.

**Acceptable synonyms**: Alternative names listed in UniProt may be added as acceptable synonyms, subject to the ambiguity rule below.

**Ambiguous alternative names**: An alternative name that applies to proteins encoded by different genes shall not be added as a synonym to any individual protein concept. This follows the principle used in HGNC gene nomenclature, whereby a name shared across multiple gene entries is omitted from all affected entries. If an alternative name is identified as ambiguous across multiple existing SNOMED CT concepts, it shall be removed from all affected concepts.

**EC numbers**: EC numbers shall not be added as descriptions to protein-level concepts. An EC number identifies an enzyme activity or reaction class, not a specific protein. Because proteins encoded by different genes may share the same EC classification, using an EC number as a synonym for an individual protein would be misleading.

**Gene names**: Gene names shall not be added as synonyms to protein concepts. A gene name identifies the gene, not its protein product. Furthermore, a gene symbol alone may not reliably distinguish between related protein products, including isoforms or paralogs.

**Protein names identical to gene names**: Where a protein name is identical to a gene name, disambiguate by appending "protein" to the protein concept name since SNOMED CT descriptions do not support italics, which is the conventional typographic distinction used in the literature.

For example,

* 1417977000 |1-acyl-sn-glycerol-3-phosphate acyltransferase beta (substance)|
* PT: 1-acyl-sn-glycerol-3-phosphate acyltransferase beta
* Synonyms:  1-acylglycerol-3-phosphate O-acyltransferase 2, 1-AGP acyltransferase 2, 1-AGPAT 2, Lysophosphatidic acid acyltransferase beta

