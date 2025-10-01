# Clinical Drug (CD) with Concentration and Presentation Strengths

Clinical drug concepts in the international edition are authored _either_ using presentation strength (for discrete dose forms) _or_ using concentration strength (for liquid dose forms and patches, etc.) as appropriate for different types of product (see [Clinical Drug with Continuous Dose Form](../medicinal-product/index/clinical-drug-with-continuous-dose-form.md), [Clinical Drug with Discrete Dose Form](../medicinal-product/index/clinical-drug-with-discrete-dose-form.md), and [Appendix A: Product Patterns](../pharmaceutical-and-biologic-product-and-dose-form-attributes-summary/appendix-a-product-patterns/)). Concentration strength in SNOMED CT is where the description of the strength of a clinical drug has been normalized such that the denominator value is "one" and the denominator unit is a unit of mass (e.g., grams) or volume (e.g., milliliters). Presentation strength is a description of the strength of the clinical drug as it is present in its unit of presentation (vial, ampoule, sachet).

By limiting the the Clinical Drug class in the international edition to expression of strength _either_ as concentration strength _or_ as presentation strength, medicinal product concepts that could usefully have _both_ concentration and presentation strength (for example, some liquid products such as liquid parenteral products or liquids for inhalation via a nebulizer) will have only concentration strength in the international edition. National extensions may author clinical drug concepts using the presentation strength(s) and unit(s) of presentation available in their jurisdiction if use case(s) require this. These concepts will be child concepts of the concentration clinical drug in the international edition. The diagrams below illustrate this:

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-10-01 at 1.01.23 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://confluence.ihtsdotools.org/download/attachments/123904097/CD%20types.png?api=v2&#x26;nonce=1756931226636" alt=""><figcaption><p>Figure: Clinical Drug concepts and their relationship together and to MPF only concepts</p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-10-01 at 1.03.16 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://confluence.ihtsdotools.org/download/attachments/123904097/CD%20types%20SCT%20notation.png?api=v2&#x26;nonce=1756931226635" alt=""><figcaption><p>Figure: Clinical Drug concepts and their relationship together and to MPF only concepts in SNOMED notation, showing optional national extension concepts</p></figcaption></figure>



<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-10-01 at 1.03.57 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://confluence.ihtsdotools.org/download/attachments/123904097/CD%20conc%20pres%20example.png?api=v2&#x26;version=2" alt=""><figcaption><p>Figure: Clinical Drug example showing optional national extension concepts</p></figcaption></figure>

In national extensions, the concentration strength clinical drug may be sufficient, or there may be a requirement to represent some, usually liquid dose form product clinical drugs, using **both** concentration and presentation strength either for the abstract clinical drug, or for the real clinical drug, or for both. This is shown in the diagram below:

<figure><img src="../../../../../.gitbook/assets/image (19) (1).png" alt=""><figcaption><p><em>Diagram of relationships and optionality for presentation strength and concentration strength Clinical Drug and Real Clinical Drug</em></p></figcaption></figure>

Even within a single jurisdiction, authorizations are not always consistent in dealing with presentation and concentration strength. Some regulatory agencies have or are moving to licensing all parenteral liquid products using presentation strength (with the exception of some products such as insulins and large volume parenteral fluid replacement products and bulk use vials, etc.); other agencies have been or are using this pattern for some products (e.g., pre-filled syringes) and may change for others as IDMP takes effect. Some national terminologies are working to normalise the patterns of strength representation particularly for safety considerations; others are dealing with the mixed economy that exists "as is". This specification provides support for the different patterns for both clinical drugs and real clinical drugs whilst maintaining the requirement that concepts will classify correctly within the system.

This modeling pattern is advised for use with usually liquid products that are placed inside a unit of presentation such as an ampoule, vial, cartridge or pre-filled syringe, which itself is then put inside a package, usually but not always with other identical units, for placement into the supply chain. For these products, the presentation strength is itself often clinically relevant, and therefore, although the fully specified name pattern (as currently described) uses the concentration strength, a synonym (which could be the preferred term for a national extension) could use the presentation strength description; for example: "enoxaparin sodium 120 milligram/0.8 millilitre conventional release solution for injection in pre-filled syringe".

As the unit of presentation is the "countable entity" of the clinical drug, this modeling pattern is not advised for continuous semi-solids (creams, ointments, etc.) or continuous liquids (oral solutions, suspensions) where there is no "countable entity". The unit of presentation should not be confused with the package for continuous semi-solids and liquids that is placed into the supply chain (tubes, bottles, etc.). The package should be described using the (R)PCD structure which describes the package size but not currently the package type. For example: chloramphenicol 5 milligram/1 milliliter conventional release eye drops are supplied in a 10mL bottle; the clinically relevant information is the "10mL" volume, which is the package size.

## Use cases

This is the pattern for a national extension to author a presentation strength representation of a clinical drug that is described using concentration strength in the international edition. This can be used for:

* liquid parenteral products presented in units of presentation, such as ampoules, vials, pre-filled syringes, cartridges, or bags/bottles
* liquid oral products presented in a sachet or other unit dose unit of presentation
* liquid pulmonary products presented in a unit dose presentation unit of presentation

In addition to the usual attributes for a concentration strength clinical drug, the unit of presentation size and unit of presentation unit attributes are used. The concept will then classify correctly as a child of the existing concentration strength clinical drug. This does mean that the exact presentation strength must be authored manually as an additional description and that the exact presentation strength is not provided in the logical definition (other than via calculation), but this pattern has been found to be the most efficient method for authoring such concepts, especially when there are multiple active ingredient substances. The alternative was to author both concentration strength and presentation strength in two role groups, which, whilst it does also give the correct classification, is very labour intensive.

## Attributes

The following attributes apply to Clinical Drug (CD) concepts in a national extension, which require both concentration and presentation strength.

| **Semantic tag**                                                  | **(clinical drug)**                                             |
| ----------------------------------------------------------------- | --------------------------------------------------------------- |
| **Definition status**                                             | <ul><li>900000000000073002</li></ul>                            |
| **Attribute:** 411116001                                          | Has manufactured dose form                                      |
| <p><br><strong>Attribute:</strong> 1142139005</p>                 | Count of base of active ingredient                              |
| **Attribute:** 763032000 \|Has unit of presentation\|             | <p><strong>Range</strong></p><ul><li>&#x3C; 732935002</li></ul> |
| **Attribute:** 1148793005                                         | Unit of presentation size quantity                              |
| **Attribute:** 320091000221107 \|Unit of presentation size unit\| | <p><strong>Range</strong></p><ul><li>&#x3C; 767524001</li></ul> |

| <p><strong>Role Group</strong><br><strong>[1..*]</strong></p><p><strong>One role group is required for each precise active ingredient</strong></p> |                                                                                                                                           |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Attribute:** 762949000 \|Has precise active ingredient\|                                                                                         | <p><strong>Range</strong></p><ul><li>&#x3C; 105590001</li></ul>                                                                           |
| **Attribute:** 732943007 \|Has basis of strength substance\|                                                                                       | <p><strong>Range</strong></p><ul><li>&#x3C; 105590001</li></ul>                                                                           |
| **Attribute:** 1142138002 \|Has concentration strength numerator value\|                                                                           | <p><strong>Range</strong></p><ul><li>DEC (decimal)</li></ul><p><strong>Cardinality</strong> (within role group)</p><ul><li>1..1</li></ul> |
| **Attribute:** 733725009 \|Has concentration strength numerator unit\|                                                                             | **Range:** < 767524001                                                                                                                    |
| **Attribute:** 1142137007 \|Has concentration strength denominator value\|                                                                         | <p><strong>Range</strong></p><ul><li>DEC (decimal)</li></ul><p><strong>Cardinality</strong> (within role group)</p><ul><li>1..1</li></ul> |
| **Attribute:** 733722007 \|Has concentration strength denominator unit\|                                                                           | **Range:** < 767524001                                                                                                                    |

{% hint style="info" %}
**Note** : The cardinalities given in the above table are for concepts in the CD class with concentration and presentation strength. These cardinalities may be stricter than those in the MRCM, which typically apply across a broader range of concepts.
{% endhint %}

Also note that the unit of presentation, the unit of presentation size quantity, and the unit of presentation size unit are not role grouped together, as there should only ever be 0..1 of each present for any one clinical drug concept.

For clinical drugs that have two or more active ingredient substances that are modifications of the same base substance, **and where** MP precisely concepts are required in the national extension, and for single ingredient product concepts where the active substance is an ingredient in these multiple modification multi-ingredient products, the following extra ingredient count attribute will be required in order to support correct relationships generated by the MRCM:

| Attribute 1142141006 \| Count of base and modification pair \| | INT (integer) 1..1 Range Cardinality |
| -------------------------------------------------------------- | ------------------------------------ |

For concepts that have two or more active ingredient substances that are modifications of the same base active ingredient substance (i.e., parent ingredient substance) **and** where one is a further modification of the other (for example, a multi-ingredient product containing both dexamethasone phosphate and dexamethasone sodium phosphate, where the dexamethasone phosphate is a modification of dexamethasone (base) and dexamethasone sodium phosphate is a further modification of the dexamethasone phosphate) **and where** MP precisely concepts are required in the national extension, and for single ingredient product concepts where the active substance is an ingredient in these multiple modification multi-ingredient products, the following extra ingredient count attribute will be required in order to support correct relationships generated by the MRCM:

| Attribute 1142140007 \| Count of active ingredient \| | INT (integer) 1..1 Range Cardinality |
| ----------------------------------------------------- | ------------------------------------ |

## Example Diagrams

Some examples of clinical drug concepts, with concentration strength and presentation strength in a national drug extension, are shown below.

**Stated template view:**

<figure><img src="../../../../../.gitbook/assets/image (20) (1).png" alt=""><figcaption><p><em>Clinical drug (CD) concentration and presentation strength for a national extension stated template view</em></p></figcaption></figure>

**Example: single active ingredient substance clinical drug with concentration and presentation strength for a national extension**

<figure><img src="../../../../../.gitbook/assets/image (21) (1).png" alt=""><figcaption><p><em>Clinical drug (CD) concentration and presentation strength for a national extension stated view</em></p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/image (22) (1).png" alt=""><figcaption><p><em>Clinical drug (CD) concentration and presentation strength for a national extension inferred view; s</em> <em>hows how the concentration and presentation strength clinical drug authored in the national extension will classify as a child of the concentration strength CD in the international edition</em></p></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Clinical%20Drug%20%28CD%29%20with%20Concentration%20and%20Presentation%20Strengths" class="button primary">Provide Feedback</a>
