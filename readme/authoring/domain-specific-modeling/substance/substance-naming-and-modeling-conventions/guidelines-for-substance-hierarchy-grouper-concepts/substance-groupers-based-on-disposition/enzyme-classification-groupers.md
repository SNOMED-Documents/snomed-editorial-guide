# Enzyme Classification Groupers

## Scope

This guidance applies to enzyme classification concepts within the substance hierarchy under 90668006 |Substance with enzyme mechanism of action (substance)|. It specifies how enzyme classes are represented as disposition groupers at all levels of the Enzyme Commission (EC) classification hierarchy. The primary reference for enzyme class names, the reaction, and alternative names is the[ IUBMB Enzyme Nomenclature database](https://iubmb.qmul.ac.uk/enzyme/).

## Modeling principle

Enzyme classes shall be represented as substance concepts with the corresponding enzymatic activity modelled as the value of the Has disposition attribute.

This principle applies consistently at all levels of the EC classification hierarchy, including:

* EC class level: EC x (e.g. EC 2 - Transferases)
* EC subclass level: EC x.y (e.g. EC 2.3 - Acyltransferase)
* EC sub-subclass level: EC x.y.z (e.g. EC 2.3.2 - Aminoacyltransferases)
* EC leaf level: EC x.y.z.n (reaction-specific entry e.g. EC 2.3.2.7 - aspartyltransferase)

The Has disposition value represents the biochemical reaction catalysed by the enzyme class. Where a disposition concept representing the required enzymatic activity does not already exist, it will be created at the appropriate level within the disposition hierarchy before the corresponding enzyme class substance concept is created.

## Naming conventions for EC class concepts

* Fully specified name (FSN): Substance with X mechanism of action, where X is the IUBMB-accepted enzyme class name.
* Preferred term (PT): The IUBMB-recommended enzyme class name.
* Acceptable synonyms: Alternative names recognised by IUBMB or supported by other authoritative primary databases may be added as synonyms, where appropriate.
* EC numbers: EC numbers shall not be added as descriptions to EC class substance concepts. The EC classification is used to identify the enzyme class and its associated catalytic activity, rather than as a synonym.

For example,

* 44121006 |Substance with transferase mechanism of action (substance)|
* PT: Transferase

