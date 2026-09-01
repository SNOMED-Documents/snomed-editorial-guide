# Organism Naming Conventions

## Fully Specified Name

The fully specified name (FSN) of organism concepts names classes that are officially recognized Linnaean taxonomic classes, and include a designation of rank (other than species).  They include, but are not limited to, Phylum, Order, Suborder, Class, Family, Genus, and subspecies.

Properly constructed FSNs contain terms indicating the taxonomic rank + the recognized name of that rank + semantic tag.

* For example,
  * 106544002 | Family Enterobacteriaceae (organism)|

{% hint style="info" %}
**Rank**

The naming convention is not applied to concepts that only refer to a subgroup of a rank.

* For example,
  * Vancomycin resistant Enterococcus (organism) is **correct** in capitalizing Enterococcus. It refers to a subclass of the genus, Enterococcus species that are resistant. Enterococcus is a scientific name of an organism class; therefore, the first letter is capitalized.
  * _Vancomycin resistant Genus Enterococcus_ is **incorrect**. It refers to the rank only, Genus Enterococcus.
{% endhint %}

#### Exclusion of parentheses and/or abbreviations in FSNs

While some references and scientific notations include details such as the subgenus and historical authority to achieve maximum precision in descriptions, SNOMED CT does not.&#x20;

Official names of organisms may include abbreviations such as “subsp.” and “subgen.” (relevant to Domain Bacteria and Kingdom Plantae).  However, the SNOMED CT fully specified names of organisms should include the expanded word for rank, i.e., “subgenus” or “subspecies”, and not an abbreviation of these terms.

* For example,&#x20;
  * |Sarcoptes scabiei variety canis (organism)| is the correctly formatted FSN, while the description with the abbreviation |Sarcoptes scabiei var. canis| is the PT.&#x20;
  * |Streptococcus equi subspecies equi (organism)| is the correctly formatted FSN, while the description with the abbreviation |Streptococcus equi subsp. equi| is the PT.&#x20;

Official names of organisms may include parentheses.  However, the SNOMED CT FSN should not include parentheses.

* For example,
  * _Cypraea (Cypraea) tigris_ would have a correctly formatted FSN of |Genus Cypraea subgenus Cypraea tigris (organism)|
  * _Bacillus (subgen. Bacillus Cohn 1872, 174) subtilis_ would have a correctly formatted FSN and PT of |Bacillus subtilis (organism)|

{% hint style="warning" %}
**Exception**

When the same Scientific Name is used in two different hierarchies (two different kinds of organisms), use the Scientific Name with annotated common name as FSN and PT to prevent confusion. A dash may be used to separate the two names. Use the common name from the authoritative source. If a common name is not listed in the authoritative source, use the NCBI BLAST name as common name in the FSN and PT. If a common name is not in either the authoritative source or in the NCBI BLAST names, consult the literature or other resources for a distinguishing name to use in the FSN and PT. Synonyms containing official scientific name (with or without taxonomic rank designation) will not be added for these concepts to avoid ambiguity and prevent duplication of the names.

* For example,
  * The genus of bacteria Edwardsiella does not have a common name listed in the authoritative source. Therefore, use the NCBI BLAST name "enterobacteria" in the FSN. For the genus of animals Edwardsiella, use the common name "sea anemones" from the authoritative source.
    * 14566004 |Genus Edwardsiella - enterobacteria (organism)|
    * 1351899003 |Genus Edwardsiella - sea anemones (organism)|

A description matching the FSN is used as PT.

Synonyms such as "Genus Edwardsiella" or "Edwardsiella" are not added as acceptable descriptions to any of the concepts.
{% endhint %}

## Preferred Term

The Preferred Term is the official scientific name.  It may include abbreviations and/or parentheses.&#x20;

* For example,
  * Cypraea (Cypraea) tigris
  * Pleione subg. Scopulorum

The preferred term usually does not include the taxonomic rank designation except for the following cases:

* Official names of organisms may include abbreviated taxonomic rank such as “subg.“ "subgen." or “subsp.”.
* In rare cases, two Linnaean taxon ranks in the same hierarchy may have the same name. For example, in Kingdom Bacteria, "Thermodesulfobacteria" is an applicable term at both Phylum and Class levels. In this case, the taxon rank is included in the preferred term to prevent any ambiguity.

{% hint style="warning" %}
**Common Name Exceptions**

1. Core Naming Principle:&#x20;
   1. The Preferred Term for an organism concept is the official scientific (Linnaean) name by default.&#x20;
   2. A common name may replace the scientific name as the PT only when all of the following criteria are satisfied:
      1. The common name is attested in a primary reference (ITIS) or a recognized secondary reference (COL, Thermo Fisher).
      2. The common name is in English. Non-English common names (e.g. French or Spanish vernacular names) must not be used as the PT. &#x20;
      3. A single common name (or grouper name) can be identified that applies unambiguously to every extant descendant of the concept. If no single term covers all descendants, the scientific name is retained as the PT.
      4. The common name is stable and widely recognized as evidenced by its use in 2 or more primary or secondary references. It should not be constructed or invented specifically to satisfy the guideline.
2. Application by Taxonomic Level
   1. Species and Genus: Common names work best at the species level  and relatively well at the genus level, where groupings are phylogenetically stable and a single name typically covers the group cleanly. The criteria in Section 1 should be used in assigning the common name as the PT wherever they are met. Examples&#x20;
      1. Genus Felis → PT: small cats (covers domestic cats, wildcats, and mountain cats; unique within Felidae)&#x20;
      2. Genus Orcinus → PT: Killer whales  (monotypic genus; term is widely established)&#x20;
      3. Genus Canis → PT: Canis  (primary references list dogs, foxes, jackals, wolves, and coyotes; no singular term encompasses all descendants; scientific name is maintained; ‘Wolf-like canines’ potentially added as synonym if referenced)
3. Family and Above
   1. At the Family level and higher, the diversity of included taxa frequently means that no single common name covers all descendants cleanly. These taxonomic ranks are particularly susceptible to phylogenetic revision as new genetic data emerges. Attaching a common name PT to  these taxons increases the maintenance burden when genera move between families, since the common name may no longer apply to all descendants. The default at these levels is to retain the scientific name as the PT. A common name (or grouper name) may be used only where section 1 criteria are met and typically will be limited to cases where a widely recognised grouper name already exists and has clinical utility. Example:&#x20;
      1. Family Cervidae → PT: Cervids (ITIS lists term as valid grouper covering all deer, caribou, moose, and wapiti)
      2. Order Columbiformes → PT: Doves and pigeons (widely recognised term with established clinical utility)
      3. Family Albulidae → PT: Albulidae (competing vernacular names exist; since no single term encompasses all descendants, scientific name is maintained. A grouper common name (a combination of vernacular names in a single synonym) can be added as synonym. For example ‘bonefishes and bananafishes’ can be added as a synonym for Family Albulidae
      4. Class Tetrapoda → PT: Tetrapoda (no singular common name identified across references)
4. Handling Multiple Common Names
   1. When a primary reference lists multiple common names for a taxon, consult secondary references (COL, Thermo Fisher) to identify the most widely used single English term.
   2. If secondary references confirm that no single English common name predominates, or that the listed names describe different subsets of the taxon, retain the scientific name as the PT and add the attested common names as synonyms.&#x20;
5. Shared Common Names
   1. Where a common name is shared between two or more organism concepts, the PT should follow the existing format: scientific name with annotated common name, separated by a dash.
      1. Example&#x20;
         1. Genus Megapodius → PT: Megapodius - megapodes&#x20;
         2. Family Megapodiidae → PT: Megapodiidae - megapodes
   2. Where a common name coincides with the scientific name of a different organism concept, the same dash-annotation convention applies to avoid ambiguity.
      1. Example Gorilla gorilla → PT: Gorilla gorilla - gorilla  (Gorilla is the scientific name for Genus Gorilla)
{% endhint %}

## Organism class variants

The description of organism classes that are subspecies subtypes and variants may include terms such as serogroup, serotype, biotype, variant, biovar, serovar, and pathovar.

* For example,
  * 698206009 | Brucella suis biovar 4 (organism)|

_Serovar_ and _serotype_ are generally synonymous, with a preference for _serovar_ in the FSN and PT unless there is an authoritative source for the organism that uses _serotype_.

{% hint style="info" %}
These guidelines should be applied to new content. Existing content may not be in compliance with this guidance; the process of correcting existing content will be carried out as time and resources permit.
{% endhint %}

The subspecies types and variants should be included in the FSN, PT and other descriptions as per terming in authoritative resource where one exists (example: see sub-sections for Salmonella serotype nomenclature as well as Streptococcus pneumoniae below). In the absence of such resources, associated scientific literature is consulted for the most common and accurate representation. Inclusion of the subspecies types and variants accurately is to avoid ambiguity when the same number or letter is used to refer to different organism variants.

* For example,
  * Without mentioning the specific variant (serogroup vs. serotype) and the nomenclature system (Danish vs. American), "Streptococcus pneumoniae 48" can refer to the following:
    * Streptococcus pneumoniae Danish serotype 48 (which is equvalent to Streptococcus pneumoniae American serotype 82)
    * Streptococcus pneumoniae American serotype 48 (which is equivalent to Streptococcus pneumoniae Danish serotype 7B)
    * Streptococcus pneumoniae serogroup 48

Abbreviations (var, var., sv, sv., bv, bv., pv, pv.) must not be used in the FSN.

## Capitalization of organism names

Official scientific names for organisms should be capitalized. The designation of rank does not require capitalization. This guideline is applicable to the organism current name as well as older names and synonyms.

* For example,
  * 426813007 | Order Acidobacteriales (organism) | has case significance of _Initial character case insensitive_.
  * 72646003 | Streptococcus equinus (organism) | contains a heterotypic synonym of "Streptococcus bovis". Both of these descriptions are scientific names of the organism, and therefore, both have a case sensitivity indicator of _Entire term case sensitive_ (CS).

{% hint style="warning" %}
**Exception**

Where the binomial format for an organism species includes capitalization of the first word, i.e., the genus name, the species name begins with a lower case letter.

* For example,
  * 24224000 | Brucella abortus (organism)|

If the species name includes any other word, it is not capitalized unless it is either a proper noun or part of a proper noun.

* For example,
  * 31989009 |Murray Valley encephalitis virus (organism)|
{% endhint %}

Capitalization is applicable to the organism scientific name, e.g., Hepatitis B virus, Buffalopox virus, Cowpox virus, Dengue virus, Herpes simplex virus 1, Herpes simplex virus 2, Herpes simplex virus 3, Human immunodeficiency virus 1 _,_ Influenza virus A, Influenza virus B, Influenza virus C, Measles morbillivirus and Measles virus, Orf virus, Rabies virus, Rubella virus, Salmonella enterica subspecies enterica serovar Typhi, Vaccinia virus, Vesicular stomatitis Indiana virus, Yellow fever virus, Human papillomavirus x (where x is number representing the serotype).

The name of the associated disease does not require capitalization, e.g., hepatitis, buffalopox, cowpox, dengue, herpes, influenza, measles, orf, rabies, rubella, typhoid, smallpox, vesicular stomatitis, yellow fever.

Non-taxonomic groupers, such as _human herpes simplex virus_ , _herpes simplex virus_ , _influenza virus_ , _human immunodeficiency virus_ , and _human papillomavirus_ are recorded with a case sensitivity indicator of _Entire term case insensitive_ (ci).

There are cases where the authoritative resources do not have an entry for the official name of an organism. For these concepts, the associated literature is referenced for naming and case sensitivity assignments.

* For example,
  * _Severe acute respiratory syndrome coronavirus 2_ is below species level and does not have an entry in the authoritative resource, International Committee on Taxonomy of Viruses (ICTV). Therefore, it is recorded with a case sensitivity indicator of _Entire term case insensitive_ (ci), since the majority of references do not capitalize “severe”.

Common names usually have case sensitivity indicator of _Entire term case insensitive_ (ci).

* For example,
  * _Domestic cat_, common name of 448169003 |Felis catus (organism)|, has case sensitivity indicator of _Entire term case insensitive_ (ci).

If the common name includes any proper nouns, or parts of proper nouns, they need to capitalized.

* For example,
  * 598003 |Vespa crabro (organism)| has the preferred /common name of _European hornet_ with the case sensitivity indicator of _Entire term case sensitive_ (CS).

## Salmonella serovar nomenclature

### Salmonella serovars with a name

Many Salmonella serovars bear a name.  These salmonella serovars have a quadrinomial format of Genus species subspecies Serovar where the serovar name is capitalized.

* For example,
  * A synonym for 114683003 | Salmonella Doel (organism) | is Salmonella enterica subsp. enterica ser. Doel

Additional descriptions, without the species and subspecies names, are in common usage for Salmonella serovars.  The antigenic formula is often included in a description as well.

* For example,
  * 656008 | Salmonella Os (organism) |
  * Salmonella 9,12:a:1,6

In SNOMED CT, the serovar name in the description should be capitalized.

{% hint style="info" %}
**Salmonella Serovars**

Salmonella serovars, without the species and subspecies names, should not be confused with binomial species names of other organisms.
{% endhint %}

### Salmonella serovars without a name

Salmonella serovars that do not have a name are represented by their antigenic formula in the FSN.

* For example,
  * 6793003 |Salmonella II 6,8:z29:1,5 (organism)|
  * 1406835004 |Salmonella enterica subspecies enterica serovar 6,8:i:- (organism)|

## Streptococcus pneumoniae

Streptococcus pneumoniae is a human pathogen whose virulence is based on its protective polysaccharide capsule. Study of the polysaccharide capsule has identified multiple serogroups and serotypes. Serotypes are defined by the chemical structure and immunologic properties of their polysaccharide; each serogroup contains one or more serotypes that elicit the same antibody response.

There are two serotype naming systems, one in the U.S. and one in Denmark. The Danish system is nearly universally accepted and preferred. For details, please refer to See Geno K A, Gilbert G L, Song J Y, Skovsted I C, Klugman K P, Jones C, Konradsen H B, Nahm M H. Pneumococcal capsules and their types: past, present, and future. Clinical Microbiology Reviews 2015; 28(3):871-899. \[[PMID: 26085553](https://www.ncbi.nlm.nih.gov/pubmed/26085553)]).

FSN and preferred term (PT) descriptions should follow the Danish naming system. When an American synonym exists, it should be added. A synonym (SYN) that matches the FSN, but does not contain the naming system can also be added.

* For example,
  * 698149000 |Streptococcus pneumoniae serotype 48 (organism)| is as follows:
    * FSN: Streptococcus pneumoniae Danish serotype 48 (organism)
    * PT: Streptococcus pneumoniae Danish serotype 48
    * SYN: Streptococcus pneumoniae American serotype 82
    * SYN: Streptococcus pneumoniae serotype 48

The guidelines for creating new concepts containing Streptococcus pneumoniae serotypes also apply to concepts in other SNOMED CT hierarchies, such as substances and procedures.

* For example,
  * 120683007 |Streptococcus pneumoniae serotype 7F antibody (substance)| is as follows:
    * FSN: Antibody to Streptococcus pneumoniae Danish serotype 7F (substance)
    * PT: Streptococcus pneumoniae Danish serotype 7F Ab
    * SYN: Antibody to Streptococcus pneumoniae Danish serotype 7F
    * SYN: Anti-Streptococcus pneumoniae Danish serotype 7F antibody
    * SYN: Streptococcus pneumoniae Danish serotype 7F antibody
    * SYN: Antibody to Streptococcus pneumoniae American serotype 51

## Influenza virus nomenclature

Follow the latest names for genus and species according to the taxonomy authority. Although the genus and species names for influenza viruses are similar, they each follow a distinct pattern, which should be used in SNOMED CT. Also, the taxonomic name of the virus should always be capitalized.

For species, the word _virus_ is included as a separate word and follows the letter designation.

* For example,
  * 407482004 | Influenza C virus (organism)|
  * 710661004 | Immunoglobulin M antibody to Influenza B virus (substance)|
  * 10674911000119108 | Otitis media caused by Influenza A virus (disorder)|

For genus, _virus_ is included in the genus name and is not a separate word.

* For example,
  * 407481006 | Genus Gammainfluenzavirus (organism)|
  * 407477006 | Genus Alphainfluenzavirus (organism)|

The disorder _influenza_ need not be capitalized.

* For example,
  * 408687004 | Healthcare associated influenza disease (disorder)|
  * 230188005 | Post-influenza encephalitis (disorder)|

## US/GB spelling variants for taxonomic concepts

Taxonomic resources (e.g. Integrated Taxonomic Information System or ITIS, List of Prokaryotic names with Standing in Nomenclature or LPSN) use the official scientific name for organisms. Similarly, in SNOMED CT, the official scientific name should be used in FSNs and PTs. **For descriptions representing common names, if the spelling in a country or region is different, the preferred spelling should be added in the language RefSet extension as a synonym.**

## Use of X species

In the context of the Linnaean organism hierarchy, there is no difference between _Salmonella species_ and simply _Salmonella_ , the genus. Terms with _X species_ , such as Salmonella species, are routinely used in laboratory reporting. They may provide additional information, other than the place of the organism in the Linnaean hierarchy. However, the intended connotation may vary from lab to lab and from organism to organism.

Since the organism concept represents a class of organisms, it cannot also represent what was, was not, or what will be done to identify the organism. Neither can it represent other information about the result. If there is additional information to report, it should be in a separate statement or comment (e.g. _further species identification pending_ or _sent to reference laboratory for further_ _identification_ or _further identification to be done if clinically_ indicated).

{% hint style="success" %}
**X species**

Addition of _X_ species as a description to genus _X_ is allowed and is done per request.
{% endhint %}

## Microorganism name changes

Microorganism taxonomic names may change, often due to scientific advances. This may result in:

* Finding an organism in a particular taxonomic group (e.g. Genus) that is unrelated, on a molecular basis, to other members of the group.
* Reassessing the taxonomic group originally established, based on phenotypic characteristics.
* Proposing to reassign the organism to a different existing or new taxonomic group.

On a case by case basis, requests for name changes are based on the following use cases:

* The name of an organism changes. This scenario is also applicable when an organism name changes on multiple occasions over time.
  * Change the FSN for affected concepts, but not the concept ID, by creating a new FSN and description. Inactivate the old FSN with an inactivation value of _Outdated_.
  * Retain the old name as a synonym.
* A single species is reclassified as multiple species. This scenario is applicable if the change in classification happens at a single point in time and is reflected as such in the authoritative resources.
  * Create the new concepts.
  * Inactivate the original concept as _ambiguous._
  * Set a _possibly equivalent to_ relationship between the old concept and the new concepts.
* Multiple species are reclassified as one. This scenario is applicable if the change in classification happens at a single point in time and is reflected as such in the authoritative resources.
  * Create a new concept.
  * Inactivate the existing concepts as _outdated_ with _replaced by_ relationships to the new concept.

## Organism life stages

Concepts in the organism hierarchy represent _fully realized_ organisms. An organism's _life cycle stage_ is a characteristic of a given taxon. It represents different stages of life e.g. egg, larva, and adult.

Organism stages themselves are characteristics common to members of a given taxon.

SNOMED CT allows for the representation of an organism in a specific life cycle stage.

* For example,
  * 337915000 |Homo sapiens (organism)| are organisms. Homo sapiens include humans, in general, as well as children.
  * Childhood is a _life cycle stage_, however it is not an organism.

Similarly,

* An egg of a particular nematode, e.g., 42625000 |Strongyloides stercoralis (organism)| is an organism. It is alive and can pass through other stages appropriate to its species.\
  However, the _egg stage_ of Strongyloides stercoralis is not an organism. Many diagnostic test results, identify organisms ‘participating’ in particular life cycle stages.

For example, the results of a 83033005 |Fecal analysis (procedure)| may identify the presence of 609326000 |Larva of Strongyloides stercoralis (organism)| and 699572004 |Egg of Strongyloides stercoralis (organism) |.

{% hint style="info" %}
**Organism concepts**

Concepts in the organism hierarchy should not represent organism _structures_ (e.g., fungal hyphae). In addition, the word "_stage"_ should be excluded from concepts representing life cycle of an organism (e.g. larval **stage** of a nematode parasite). This does not preclude representations of organisms ‘participating’ in a specific stage of life e.g., 609061000 |Larva of genus Ascaris (organism)|.
{% endhint %}

### Naming patterns

FSN pattern: (Life cycle stage) of (Taxon including rank, if required) (organism)

* For example,
  * 609043009 | Adult of phylum Nemata (organism)|
  * 699572004 | Egg of Strongyloides stercoralis (organism)|

The name of the rank is included with the first letter lower case, except at the species and subspecies levels, where the Linnaean binomial and trinomial are specified.

PT pattern: (Taxon including rank, if required) (life cycle stage)

* For example,
  * Phylum Nemata adult
  * Strongyloides stercoralis egg

#### Cestode larvae

A number of _cestode larvae_ have historically been referred to using Linnaean binomial names that are completely different from corresponding adult (or egg) names.

* For example,
  * 47399003 | Larva of Taenia saginata (organism) |, a human tapeworm, is usually called Cysticercus bovis.

PT pattern: Linnaean binomial of larva OR (Taxon including rank if required) (life cycle stage)

*   For example,

    * Cysticercus bovis
    * Cysticercus cellulosae
    * Class Cestoda larva

    Although rare, a subtype of cestode larva may appear to be a Linnaean trinomial name. This, then, is the PT:

    * Diphyllobothrium latum sparganum

#### Other acceptable synonyms

Some organisms and stages are referred to in an _adjectival_ form (e.g., Ascarid egg) or by common name (e.g., adult nematode). When used (especially when described as part of a request), these terms may be included as additional synonyms.

## Homotypic and heterotypic synonyms

Homotypic synonyms (also referred to as objective or nomenclatural or obligate synonyms), sometimes indicated by a triple bar <img src="../../../../.gitbook/assets/image (101).png" alt="" data-size="line">, are based on the exact same type specimen. These synonyms are published in the scientific literature following the formal nomenclatural rules (that is, they are declared through a _nomenclatural_ _act_).

Heterotypic synonyms (also referred to as subjective or taxonomic synonyms), sometimes indicated by “=“, are based on different type specimens. These synonyms rely on the opinions of taxonomists rather than on the formal nomenclatural rules.

In SNOMED CT, homotypic synonyms can be added as descriptions on concepts as per primary references and the various International Codes of Nomenclature. Additional synonyms are expected to be referenced in current literature. Heterotypic synonyms can be added to aid search and analysis; they would only be considered for addition if requested and are supported by a primary resource, e.g. LPSN. They should not be added if adding them would generate confusion.

## Dual nomenclature of pleomorphic fungi

According to the _International Code of Nomenclature for algae, fungi, and plants_ (IAPT), as of 1 January 2013, the historical system of permitting separate names for anamorphs and telemorphs of fungi with a pleomorphic lifecycle was ended, and one fungus can only have one name. All legitimate names proposed for a species, regardless of what stage they are typified by, can serve as the correct name for that species. It has been recognized that there could be many names that might merit formal retention or rejection, and the problem of choosing one name among many remains to be examined for many species. Therefore, latest updates in the credible resources and/or scientific articles should be consulted for the most current name.

## O Rough bacteria

There is currently no standard approach in authoritative sources for naming rough bacterial strains. Multiple representations of _rough_ organisms exist in the literature; however, in the absence of a formal standard, SNOMED International has adopted the notation “O rough” for the fully specified name and preferred term of new content.

* For example,
  * 720764004 | _Yersinia enterocolitica_ serogroup O rough (organism)

Alternative representations, such as _O-rough_, _rough_, or _Orough_, may be included as synonyms when use case requires.

## Resources for organism naming

SNOMED International utilizes various resources when reviewing changes to the organism hierarchy. They include:

### Bacteria

* List of Prokaryotic names with Standing in Nomenclature (LPSN)
* International Committee on Systematics of Prokaryotes (ICSP)
* International Journal of Systematic and Evolutionary Microbiology
* DSMZ-Prokaryotic Nomenclature Up-to-date

### Fungi

* MycoBank Database
* Index Fungorum

### Viruses

* International Committee on Taxonomy of Viruses (ICTV)

### Parasites

* Integrated Taxonomic Information System (ITIS)

### Protozoa

* National Center for Biotechnology Information (NCBI) Taxonomy. Although not an authoritative source, NCBI Taxonomy provides useful links to other sources; it is used by Unified Medical Language System (UMLS) as a QA source.

### General

* Catalogue of Life. &#x20;
  * This is the result of cooperation between ITIS and Species 2000.  Catalogue of Life may not be up to date for all areas. For bacteria, fungus, and virus, consult resources noted above as primary references.
* International Code of Zoological Nomenclature (ICZN)
* International Code of Nomenclature for algae, fungi, and plants (IAPT)

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Organism%20Naming%20Conventions" class="button primary">Provide Feedback</a>
