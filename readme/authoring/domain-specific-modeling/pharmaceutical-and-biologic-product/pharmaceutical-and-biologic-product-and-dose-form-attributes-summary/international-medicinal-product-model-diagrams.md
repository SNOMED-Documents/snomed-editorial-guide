# International Medicinal Product Model Diagrams

## **Medicinal Product model diagrams**

The diagrams below show the overall basic medicinal product model. Note that in each diagram, no role, structure, or disposition grouper concepts are shown. Definitions and detailed descriptions are given in the sections following this overall model introduction.

MP classes = shades of blue

MPF classes = shades of yellow

CD class = green

This first diagram is a class model illustrating the five classes of concepts in the model and the relationships between them, in their three groups (MP, MPF and CD) plus an additional optional sixth sub-class to be populated in limited cases and likely in national extensions only (MP Precise Only). Two classes use the existential restriction (MP and MPF) and four use the (proxy for the) universal restriction (MP only, MPF only, CD and MP Precise Only). MP Precise Only is the optional sub-class that represents a product described explicitly and only by its _precise_ active ingredient substances, i.e. including clinically significant modification such as "dexamethasone _sodium phosphate_ ".

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-09-26 at 1.34.08 PM.png" alt=""><figcaption></figcaption></figure>

<p align="center">Figure: Medicinal Product concept model - International edition</p>

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-09-26 at 1.35.36 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/304775774.png" alt=""><figcaption><p>Figure: An example of Medicinal Product - International edition</p></figcaption></figure>

The next diagram below is in SNOMED notation (inferred view), and shows only the five classes that will be populated in the international release, at least for the foreseeable future.\
The Medicinal Product model is parented by the proximal primitive 763158003 |Medicinal product (product)| concept, an abstract concept representing an item that "has been formulated and manufactured for administration to humans (or animals) for treatment or prevention of disease, for diagnosis of illness or to restore, correct or modify physiological function and which contains an active ingredient substance or combination of substances". This parent concept acts both to scope the domain and, in the future, will separate medicinal products from other products in a larger Products hierarchy, which may include medical devices and certain other products such as foods and cosmetics.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-09-26 at 1.36.33 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/304775772.png" alt=""><figcaption><p>Figure: Medicinal Product concept model - International - SNOMED notation</p></figcaption></figure>

The last model diagram below shows multi-ingredient medicinal products, and therefore, has increased complexity. It again shows the three groups (MP, MPF and CD) with MP classes shown in shades of blue, MPF classes in shades of yellow and the CD class in green; each with two single active ingredient representations (X and Y) and one multi-ingredient representation (X + Y) and then the relationships between these. It shows how the single ingredient "containing" classes (the open world classes) subsume the appropriate multi-ingredient class, whereas the single ingredient "containing only" classes (the closed world classes) do not subsume the multi-ingredient class. The optional MP Precise Only class is present but is not shown with any multi-ingredient products, to limit complexity. MP Precise Only multi-ingredient products are discussed later in the [Ingredient Count Attributes](ingredient-count-attributes.md).

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-09-26 at 1.38.17 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/304775776.png" alt=""><figcaption><p>Figure: Medicinal Product concept model - International - showing multi-ingredient concepts</p></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-09-26 at 1.40.12 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../authoring/pharmaceutical-and-biologic-product/images/304775765.png" alt=""><figcaption><p>Figure: Example of multi-ingredient concepts - ezetimibe and simvastatin</p></figcaption></figure>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=International%20Medicinal%20Product%20Model%20Diagrams" class="button primary">Provide Feedback</a>
