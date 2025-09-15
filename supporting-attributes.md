# Supporting Attributes

The section describes the attributes used in the definition of the concepts classes in the national extension model.

# Has product name

## Definition

The (authorised) product name for the medicinal product as designated by the license holder (supplier); this may (or may not) be a trademarked name, and is often referred to as the _brand name_. 

## Discussion

The [ 774158006 | Has product name (attribute)|](http://snomed.info/id/774158006 "774158006 | Has product name \(attribute\) |") is used in the definition of the real medicinal product and the real clinical drug. It is not used in the real packaged clinical drug, as this brings the relevant information via the real clinical drug it contains.

It is not essential that the product name be an invented or brand name; it can be a generic name (for example, using one or more international non-proprietary therapeutic substance names). The product name concepts are authored to value the definitional attribute for the real medicinal products and real clinical drugs in the national extension, and since real packaged clinical drugs contain real clinical drugs, this set of concepts does also. 

It is possible for an extension that wishes to author a hierarchy of product name concepts to choose to value the [ 774158006 | Has product name (attribute)|](http://snomed.info/id/774158006 "774158006 | Has product name \(attribute\) |") differently for the different classes of real medicinal product and real clinical drug. 

For example,

<figure><img src="images/308610857.png" alt="" title=""><figcaption><p><em>Figure 1: Diagram of examples of a product name hierarchy</em></p></figcaption></figure>

In a product name hierarchy, the parent product name concept should be authored to reflect the unique set of active ingredient substances for the real medicinal product and associated real clinical drug concepts. It is therefore most useful if the parent product name does not include any reference to dose form (e.g., "LA" or "Retard") or to strength (e.g., "Double Strength") or any other information such as indication (e.g., "Shingles Treatment"). Child product name concepts can be authored to include additional information as provided in the authorised name for real clinical drugs. 

Product name concepts must be authored in each national extension since the same product name can represent products containing different active ingredients in different jurisdictions, and therefore, the product name can have a different meaning in different jurisdictions. 

The [774158006 |Has product name (attribute)|](https://browser.ihtsdotools.org/?perspective=full&conceptId1=774158006&edition=MAIN/2021-07-31&release=&languages=en) is available from the concept model attribute hierarchy; values for [ 774158006 | Has product name (attribute)|](http://snomed.info/id/774158006 "774158006 | Has product name \(attribute\) |") should be authored in the national extension using the root of  [ 774167006 | Product name (product name)|](http://snomed.info/id/774167006 "774167006 | Product name \(product name\) |") from the Qualifier hierarchy.  

# Has supplier

## Definition

The (name of the) organisation that holds the authorisation for marketing or supply of the medicinal product. 

## Discussion

The [ 774159003 | Has supplier (attribute)|](http://snomed.info/id/774159003 "774159003 | Has supplier \(attribute\) |") is used in the definition of the real medicinal product and the real clinical drug. It is not used in the real packaged clinical drug, as this brings the relevant information via the real clinical drug it contains.

Medicinal products, like other complex products, are rarely _manufactured_ by one single organisation; the substances in a product may be sourced from a range of specialist manufacturers and then assembled into the manufactured dose form by another organisation. The assembling organisation may be a contract manufacturer holding a manufacturing license and working for a variety of clients. In ISO 11615:2017, the _manufacturer_ of a medicinal product is defined as the "organisation that holds the authorisation for the manufacturing process", and it notes that "establishment is a synonym of manufacturer". _Establishment_ is a term that is often used in the USA. In national terminologies for clinical use, however, the term _manufacturer_ usually refers to the organisation whose name and details are associated with the professional and public facing information about the product. To avoid confusion in this specification, the term _manufacturer_ has not been used; instead , _supplier_ is the term used and is the organisation responsible for providing the clinical information to support the product use both for patients and healthcare professionals and is also responsible for the quality and safety of the product, including management of all adverse event information relating, or possibly relating to, the product in use. All of those are the responsibility of the organisation that is authorised to _supply_ the product into the supply chain. Some healthcare cultures allow agreements whereby an organisation may obtain stocks of a medicinal product and then to repackage or relabel that medicinal product and place it into the supply chain, either within a single jurisdiction or across a group of jurisdictions. In this case, the repackaging/relabeling organisation is acting as a supplier, and their name and details are likely to be present on the packaging, either exclusively or in addition to the primary organisation. In these cases, the responsibility for the product information and the product quality and safety is shared in various ways depending on the agreement and jurisdictional regulations.

Nations/affiliates must decide the principles under which to populate the [774159003 |Has supplier (attribute)|](https://browser.ihtsdotools.org/?perspective=full&conceptId1=774159003&edition=MAIN/2021-07-31&release=&languages=en), based on their own regulations and context of practice. The simplest rule is to use the company who holds the authorisation to market the medicinal product; but as described above, there can be complexities. 

Issues to consider are:

  * Whether repackaging or relabeling is allowed by regulation and whether this is internal to the jurisdiction (as in the USA) or external to the jurisdiction (sometimes known as _parallel_ _importing_ or sale of _grey products_ in Europe) or whether both are allowed, and how the authorisations for these are managed and therefore which organisation (the licensed repackager or the marketing authorisation holder) to designate as the manufacturer/supplier
  * The role of the manufacturer/supplier information and the use case(s) to be supported, which may include
    * Contact for queries from clinicians and/or patients
    * Pharmacovigilance and product safety
  * Whether the national medicines terminology will include medicines not authorised in their jurisdiction, and if so, how they wish to provide manufacturer/supplier information for these
    * For medicinal products licensed outside the jurisdiction, reference to the manufacturer is still likely to be appropriate
    * For compounded specials, to reference a generic _specials manufacturer_ concept is possible since most of these will hold an authorisation to undertake specials manufacture

Due to the nature of the domain where either individual products or whole product sets, with their brand name and authorisation, can be sold from one organisation to another, it may be that even within one jurisdiction a single product name will be associated with more than one supplier. For those extensions that populate the real medicinal product concept class, in situations where individual real clinical drugs share the same product name but have different supplier organisations, two real medicinal products will exist, as shown in the example below:

<figure><img src="images/308610856.png" alt="" title=""><figcaption><p><em>Figure 2 : Diagram to show RCDs sharing a single product name associated with different RMPs due to having different suppliers</em></p></figcaption></figure>

The [774159003 | Has supplier (attribute) |](https://browser.ihtsdotools.org/?perspective=full&conceptId1=774159003&edition=MAIN/2021-07-31&release=&languages=en) is available from the concept model attribute hierarchy. Supplier organisations, by virtue of being corporate bodies and legal entities, are unique to a given nation and must have their representation authored within the national extension using [774164004 | Supplier (supplier) |](https://browser.ihtsdotools.org/?perspective=full&conceptId1=774164004&edition=MAIN/2021-07-31&release=&languages=en) from the Qualifier hierarchy as the root concept.

# Count of clinical drug type

## Definition

The number (count) of of distinct clinical drug (concepts) present in the package. For all non-combination packages, this value should be "one".

## Discussion

The [ 1142143009 | Count of clinical drug type (attribute)|](http://snomed.info/id/1142143009 "1142143009 | Count of clinical drug type \(attribute\) |") is used in the definition of the packaged clinical drug and the real packaged clinical drug. 

Count attributes are used for all medicinal product and package concepts that must be represented using the closed world view as a proxy for and until a more expressive description logic becomes available to properly represent the universal restriction. Packaged medicinal products must be described as containing _only_ those clinical drugs that are stated in the logical definition; no other content is to be contemplated (no open world view). A package containing 500mg paracetamol tablets must contain explicitly and only 500mg paracetamol tablets (not paracetamol capsules, or paracetamol and codeine tablets). To correctly describe this, and particularly to ensure that pack concepts classify correctly, so that packs that contain more than one (type of) clinical drug (i.e. combination packs) do not classify as children of packs that contain only one type of clinical drug, it is necessary to use a _clinical drug count_. This follows a similar pattern to the use of the active ingredient count attribute used for MP only concepts, MPF only concepts, and clinical drug concepts. 

By using a _count_ attribute in the definition of closed world concepts, the count information is machine processable, and therefore if/when a more expressive description logic becomes available to properly represent the closed world view, then all the count attributes can be used to transfer to the closed world description logic consistently.

Standard packs containing a single clinical drug type have a count of "one" for the [ 1142143009 | Count of clinical drug type (attribute)|](http://snomed.info/id/1142143009 "1142143009 | Count of clinical drug type \(attribute\) |") .

Combination packs have the appropriate count (always greater than one) for the number of clinical drug types present in the combination pack. If one of the components of a combination pack is a therapeutically inactive diluent, national extensions can choose whether to include this in the "count of clinical drug" and therefore whether the pack containing the diluent will classify as a sibling or as a child of any pack not containing a diluent. 

# Contains clinical drug

## Definition

The (real) clinical drug contained in the packaged product. 

## Discussion

The [ 774160008 | Contains clinical drug (attribute)|](http://snomed.info/id/774160008 "774160008 | Contains clinical drug \(attribute\) |") is used in the definition of the packaged clinical drug and the real packaged clinical drug. 

For packaged clinical drug concepts, the [ 774160008 | Contains clinical drug (attribute)|](http://snomed.info/id/774160008 "774160008 | Contains clinical drug \(attribute\) |") should be valued with a clinical drug from the international release or from the national extension (for example, if a liquid presentation has concentration and presentation strength clinical drug representation in the national extension).

For real packaged clinical drug concepts, the [ 774160008 | Contains clinical drug (attribute)|](http://snomed.info/id/774160008 "774160008 | Contains clinical drug \(attribute\) |") should be valued with a real clinical drug from the national extension.

As noted in the attribute tables for packaged clinical drug and real packaged clinical drug, it is not possible currently to explicitly specify an expression to describe the range of (real) clinical drugs to populate this attribute since (for example) a range cannot currently recognise a set of concepts with a particular semantic tag. Alternative range expressions could be developed based on the attributes that are unique to a (real) clinical drug. For example:

  * For clinical drugs: all products with a dose form, precise ingredient substance, and basis of strength substance
  * For real clinical drugs: all products with a dose form, precise ingredient substance, basis of strength substance, product name, and supplier name.

# Has pack size and Has pack size unit

## Definition

Has pack size: The amount or quantity of clinical drug present in the package

Has pack size unit: The unit of measure appropriate for the pack size

## Discussion

For (real) clinical drugs described with a unit of presentation and either a presentation strength or and concentration and presentation strength, the pack size reflects the number of units of presentation present in the package, and the pack size unit relates to the unit of presentation. For (real) clinical drugs with a continuous dose form, described with concentration strength, the pack size is the amount of the clinical drug present in the package with pack size units of either weight or volume as appropriate.

The following table describes some patterns and gives examples:

| Product type | CD strength type | Unit of presentation | Pack size | Pack size unit |
|---|---|---|---|---|
| Discrete dose forms: tablets, capsules, pessaries, suppositories etc. | presentation strength | basic dose form | number of units of presentation present in package | same as unit of presentation |
| Bendroflumethiazide 5mg conventional release oral tablet 28 pack |   | tablet | 28 | tablet(s) |
| Discrete dose forms: s achets, ampoules, vials containing powders, granules etc | presentation strength | "intimate container" - sachet, vial etc. | number of units of presentation present in package | same as unit of presentation |
| Cefotaxime 2g (per vial) powder for solution for injection 10 vial pack |   | vial | 10 | vial(s) |
| Metered dose forms: pressurised inhalers, cutaneous sprays, nasal sprays etc. with a metered dose valve | presentation strength | actuation | number of units of presentation present in package | same as unit of presentation |
| Beclometasone dipropionate 100 mcg per actuation pressurised inhalation 200 actuation inhaler |   | actuation | 200 | actuation(s) |
| Liquid dose forms: parenteral liquids, unit dose nebuliser solutions etc. in an "intimate container" | concentration strength and presentation strength) | "intimate container" | number of units of presentation present in package | same as unit of presentation |
| Metoclopramine hydrochloride 5 mg per 1 mL solution for injection 20mL ampoule 5 ampoule pack |   | ampoule | 5 | ampoule(s) |
| Liquid products described using concentration strength but which have a unit of presentation | concentration strength | "intimate container" | number of units of presentation present in package | same as unit of presentation |
| Insulin human soluble 100 unit per mL solution for injection 3mL cartridge, package of 5 cartridges |   | cartridge | 5 | cartridge(s) |
| Continuous preparation No unit of presentation exists | concentration strength | NA | Quantity of product in package | unit of measure for quantity (volume or weight) |
| Hydrocortisone 10mg/1g cutaneous cream 30g (tube) |   | NA | 30 | grams |

