# Ingredient Substance Attributes

The following sections discuss the attribute concepts used to represent the ingredient substances of concepts in the medicinal product hierarchy.

## **Ingredient Substances**

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-09-26 at 1.50.47 PM.png" alt=""><figcaption></figcaption></figure>

<p align="center">Figure: Ingredient role attributes</p>

The diagram above shows the relationship of the various attribute roles that a substance can play in the definition of MP, MPF and CD description of medicinal products. Any concept from the Substance hierarchy may play one or more of these roles within a product. In all of the descriptions below, when the phrase "a set of substances" is used, the set may have only one member.

### **Has ingredient**

A medicinal product concept has a set of substances that are combined to manufacture the medicinal product that can be described using the "has ingredient" attribute. However, each substance(s) in the "has ingredient" set will have more specific ingredient role that should be described using that more specific concept. Therefore, this is a grouping concept that is not used for definition of medicinal product concepts in the medicinal product hierarchy; it is a parent concept and it provides scope for further child concepts to be added to support future use cases, such as the description of inactive/excipient ingredient substances in products in a national extension. The physical presence or otherwise of an ingredient substance in the finished product may not explicitly be necessary for it to be part of the product's substance description; for example substances that play a role in the manufacturing process, such as solvents etc. are deemed "ingredients" for the product; their presence may or may not remain in the manufactured item. As such, basis of strength substance could be considered as a child concept of the Has ingredient concept, although it is not modeled in that way currently.

### **Has active ingredient**

A medicinal product concept has a set of active ingredient substance(s) responsible for providing the therapeutic effect of the medicinal product and which are described using the clinically relevant part or whole of the substance that is intended to have a therapeutic action on or within the body. In the majority of cases, this description excludes modifiers such as esters, salts or other non-covalent derivatives (such as a complex, chelate etc.), but may include them in the minority of cases when clinically significant (e.g. liposomal substances). This is therefore usually an abstract representation of the active ingredient substance(s) and is used in more abstract representations of medicinal products, such as MP (containing).

Note that "clinical significance" can be described as "something that has a practical, demonstrable effect on the treatment and condition of the patient". For example: different modifiers of a particular active moiety have clinical significance if they affect the potency of the therapeutic action of the moiety (and therefore have an affect on the dose quantities to be used). See Kazdin, E The Meanings and Measurement of Clinical Significance _Journal of Consulting and Clinical Consulting_ 67 (3): 332–9[1](https://prod-confluence.ihtsdotools.org/display/DOCEG/Ingredient+Substance+Attributes#Footnote1) \*\*\
\*\*This is the attribute role that is used in the definition of the MP concept (containing and only) and the MPF concept.\
Examples of substances playing the role of active ingredient in a medicinal product:

* azithromycin where the precise active ingredient may be azithromycin hemiethanolate, azithromycin isopropanolate
* haloperidol where the precise active ingredient may be haloperidol hydrochloride, haloperidol decanoate, haloperidol lactate
* esomeprazole where the precise active ingredient may be esomeprazole magnesium, esomeprazole sodium
* oxybutynin where the precise active ingredient may be oxybutynin chloride or oxybutynin xinafoate
* diclofenac where the precise active ingredient may be diclofenac sodium, diclofenac potassium, diclofenac diethylamine
* axitnitib where the precise active ingredient substance is also axitinitib

### **Has precise active ingredient**

A medicinal product concept has a set of precise active ingredient substance(s), those substance(s) that provides the therapeutic effect of the medicinal product and which are described using the fullest and most specific description of the substance _as it is used in the product(s) that the concept represents_ (as they are presented by the manufacturer in the manufactured dose form, before any dilution or transformation). The precise active ingredient substance may include various modifiers, such as salts, esters and/or polymers (e.g. pegylation); not all substances, even when used as the precise active ingredient substance, have a modification (see axitnitib). This is the attribute role that is used in the definition of the MP (precisely) concept, and in the definition of the CD (precisely).\
Examples:

* haloperidol decanoate
* oxybutynin chloride
* dexamethasone sodium phosphate
* sorafenib tosylate
* axitinib

The precise active ingredient attribute will use the Substance hierarchy as a flat list (without role chaining), so that a Clinical Drug containing a modified substance is not subsumed under a clinical drug containing the unmodified substance, thereby unintentionally adding more recursion to the clinical drug class (for example: so that a morphine (base) precise clinical drug does not subsume a clinical drug containing precisely morphine sulphate). This highlights the difference between the semantic of "contains precisely" which explicitly and exclusively describes the full modified substance in the medicinal product concept and "contains only" which inclusively describes the therapeutically active moiety which may be manifest in one or more substance modifications of itself.

Examples:

* "contains dexamethasone only" means that a product will contain only dexamethasone as its active ingredient; but that dexamethasone may be present as dexamethasone base, as dexamethasone phosphate, dexamethasone sodium phosphate, as dexamethasone acetate, as dexamethasone palmitate etc.
* "contains dexamethasone phosphate only" means that a product can contain either dexamethasone phosphate or dexamethasone sodium phosphate (which is a modification of dexamethasone phosphate) as its active ingredient; but it will not contain dexamethasone acetate or dexamethasone palmitate etc.
* "contains dexamethasone phosphate precisely" means that a product will contain exclusively dexamethasone phosphate; dexamethasone sodium phosphate will not be present

See also the subsection below "Using the ingredient roles" which provides a diagram further describing the use of role chaining with the active ingredient role and that there is no role chaining for the precise active ingredient role.

### **Basis of strength substance**

A medicinal product clinical drug concept has one or more substances that have the role of being the substance against which the strength quantity(s) of the product(s) are measured. There will be a basis of strength substance stated for each active ingredient substance present in a multi-ingredient clinical drug product.

Examples:

* azithromycin - in an oral suspension containing azithromycin hemiethanolate, where the strength is 100 mg per 5 mL of azithromycin
* haloperidol in a solution for injection containing haloperidol decanoate, where the strength is 250 mg per 5 mL of haloperidol
* esomeprazole - in a prolonged release tablet containing esomeprazole magnesium, where the strength is 20 mg per tablet of esomeprazole
* oxybutynin chloride – in an oral tablet containing oxybutynin chloride, where the strength is 5 mg per tablet of oxybutynin chloride
* paroxetine – in an oral tablet containing paroxetine hydrochloride, where the strength is 10 mg per tablet of paroxetine
* dexamethasone phosphate – in a solution for injection containing dexamethasone sodium phosphate, where the strength is 4 mg per 1 mL of dexamethasone phosphate
* diclofenac sodium – in a gastro-resistant tablet containing diclofenac sodium, where the strength is 25 mg per tablet of diclofenac sodium
* sorafenib – in an oral tablet containing sorafenib tosylate, where the strength is 200 mg per tablet of sorafenib

Almost always, the basis of strength substance is either the active ingredient substance or the precise active ingredient substance; very occasionally products are licensed using a "reference" basis of strength substance (e.g. a product containing diclofenac diethylammonium as its precise active ingredient substance having its strength expressed in terms of diclofenac sodium).

### **Using the ingredient role**

The Medicinal Product and Medicinal Product Form use the active ingredient attribute, which will have a role chain attached to it, so that it can use the Substance hierarchy as a hierarchy through the "is modification" relationship. This allows the classifier to make the appropriate relationships between MPs, MPFs and CDs based on their active ingredient substances. The role chain is a characteristic that is not inherited, so the precise active ingredient attribute does not inherit this characteristic. The Clinical Drug uses the precise active ingredient attribute/relationship which will use the Substance hierarchy as a flat list without role chaining, so that a clinical drug containing a modified substance is not subsumed under a clinical drug containing the unmodified substance, thereby unintentionally adding more recursion to the clinical drug class (for example: so that a morphine (base) precise clinical drug does not subsume a clinical drug containing precisely morphine sulphate).

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-09-26 at 1.54.26 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/304775801.png" alt=""><figcaption><p>Figure: Ingredient role chaining</p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-09-26 at 1.54.50 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/304775799.png" alt=""><figcaption><p>Figure: Ingredient role chaining example</p></figcaption></figure>

### **IDMP Compatibility**

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-09-26 at 1.55.01 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/304775803.png" alt=""><figcaption><p>Figure:  Ingredient role in ISO 11615 of IDMP</p></figcaption></figure>

Ingredient role is a specific attribute in ISO 11615 in IDMP, but no vocabulary/value set was specified in the conceptual standard for the ingredient roles. Examples that have been given include "active", "inactive" and "adjuvant". This supports the regulatory listing of all the substances present in a product, with their basic role (therapeutic or otherwise).

\
The explicit use of ingredient roles in the medicinal product model is compatible with the IDMP conceptual model; however, the relationship of ingredient role to substance strength is still being elucidated in IDMP. Note that the concept of "basis of strength substance", in the very few cases where it is not actually a substance present in the product, is managed by the use of the Reference Substance class in IDMP. See also [IDMP Compatibility for Clinical Drug](../medicinal-product/index/#idmp-compatibility).

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Ingredient%20Substance%20Attributes" class="button primary">Provide Feedback</a>
