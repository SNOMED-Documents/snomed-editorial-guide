# Organism

Definition| Examples  
---|---  
Organisms of significance to human medicine| 

  * [ 3265006 | Genus Candida (organism)|](http://snomed.info/id/3265006 "3265006 | Genus Candida \(organism\) |")
  * [ 710877000 | Beta lactam resistant bacteria (organism)|](http://snomed.info/id/710877000 "710877000 | Beta lactam resistant bacteria \(organism\) |")

  
  
## Addition of new organism concepts

Concepts that are in scope for international release and are supported by preliminary references will be added to the organism hierarchy. Upon addition of any new concept, if the immediate parent is missing, it will be added along with the requested concept.

## Organisms with qualifiers

When modeling organisms with qualifiers, the qualifier should be placed in front of the organism name.

### Morphology qualifiers

For example, a non-Linnaean class of bacteria described by morphology

  *     * [ 8745002 | Gram-positive bacterium (organism)|](http://snomed.info/id/8745002 "8745002 | Gram-positive bacterium \(organism\) |")
    * [ 416983001 | Helical Gram-negative bacillus (organism)|](http://snomed.info/id/416983001 "416983001 | Helical Gram-negative bacillus \(organism\) |")

### Physiology qualifiers****

For example, a non-Linnaean class of bacteria described by physiology

  *     * [ 59343002 | Anaerobic bacteria (organism)|](http://snomed.info/id/59343002 "59343002 | Anaerobic bacteria \(organism\) |")
    * [ 417454003 | Non-motile Salmonella (organism)|](http://snomed.info/id/417454003 "417454003 | Non-motile Salmonella \(organism\) |")

### Resistance / susceptibility qualifiers

For example, A non-Linnaean class of bacteria described by antimicrobial susceptibility

  *     * [ 712662001 | Carbapenem resistant Enterobacteriaceae (organism)|](http://snomed.info/id/712662001 "712662001 | Carbapenem resistant Enterobacteriaceae \(organism\) |")
    * [ 417943000 | Methicillin susceptible Staphylococcus aureus (organism)|](http://snomed.info/id/417943000 "417943000 | Methicillin susceptible Staphylococcus aureus \(organism\) |")

### Growth morphology

Growth morphology is not an _always and necessarily true_ characteristic of an organism and therefore should not be considered an intrinsic characteristic. The terms representing growth morphology such as _Branching Gram-positive bacillus present_ or _Gram-positive cocci in chains present_ are usually used for reporting a visual finding that is a characteristic of a sample. These terms should be represented as findings.

For example, 1231428004 |Beaded branching Gram-positive bacilli present (finding)|

## Validity

A number of qualifiers might be valid (e.g. aerobic microaerophilic, motile curved gram-negative bacteria). To determine the sequence, the decision-making process is stepwise as follows: 

  * Determined on a case-by-case basis
  * Highly dependent on fitting in with the model limitations
  * Based on  _Bergey’s Manual of Systematic Bacteriology_ as the primary reference

When requesting a new qualifier, an acceptable reference must be provided. Concepts with valid qualifiers are added to the International Release. 

## Organism groupings

Only authoritative taxonomic groupings are added to the SNOMED CT International Release. When requesting new organism concepts, authoritative references must be provided. Acceptance is determined on a case-by-case basis by authors. These concepts may evolve over time as the names evolve.

## Biotype, Serotype, Serogroup

Requests for new concepts are evaluated on a case-by-case basis.

It is important to understand the meaning from the requestor and determine how it can be modeled.

These concepts may evolve over time as the names evolve.

## X-like Organism

"X-like” organism is a term construction used in the medical lexicon that is outside the classic Linnaean taxonomy. ”X-like” organisms are identified by their similarity to some other organism. There is no single category or use of X-like organism terms; the meaning of these terms is context-dependent and open to interpretation when no context is provided. For many of these terms, the meaning will change with time. In some cases, this leads to a chain of terms that remains in colloquial use but loses value and place in the scientific literature. In addition, while reporting X-like organisms is clinically significant—unlike “untypeable” concepts—they cannot have a specific parent. These concepts are added:

  * only if clear context is provided by the requester; and
  * under the highest level concepts in the “organism” hierarchy i.e. direct parents would be Virus, Bacteria, Fungus.

## Provisional serotypes

Provisional serotypes, i.e. serotypes that have been defined but not given a number in the antigenic schema, are considered for addition on an ad hoc basis and only if it can be confirmed that this is a reproducible assignment not being duplicated by multiple organizations.

## Multidrug-resistant, extensively drug-resistant, pan drug-resistant bacteria 

SNOMED International adopted the recommendations of a joint initiative of the European Centre for Disease Prevention and Control (ECDC) and the CDC for the characterization of the different patterns of resistance found in healthcare-associated, antimicrobial resistant bacteria. A panel of international experts convened and drafted a proposal which provides clear consensus definitions. Please refer to the following article for details: Magiorakos, A. Srinivasan, A. Multidrug-resistant, extensively drug-resistant and pandrug-resistant bacteria: an international expert proposal for interim standard definitions for acquired resistance. _Clinical Microbiol Infect_ 2012; 18: 268-281.
