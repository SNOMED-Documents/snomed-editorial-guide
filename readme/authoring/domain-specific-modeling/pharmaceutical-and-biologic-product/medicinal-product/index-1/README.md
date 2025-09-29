# Medicinal Product and Medicinal Product Forms

When a clinical drug is created, the following supertypes must either already exist or must be created:

{% content-ref url="medicinal-product-containing-only.md" %}
[medicinal-product-containing-only.md](medicinal-product-containing-only.md)
{% endcontent-ref %}

{% content-ref url="medicinal-product-containing.md" %}
[medicinal-product-containing.md](medicinal-product-containing.md)
{% endcontent-ref %}

{% content-ref url="index/" %}
[index](index/)
{% endcontent-ref %}

For example,

1172863005 Paracetamol 1 g oral tablet has the following supertypes:

<figure><img src="../../../../../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

These concepts in the International Release, their descriptions, and their| Has active ingredient (attribute)| value, represent the **base** ingredient, not a modification.

For example,

1204319004 |Product containing precisely retinol (as retinol palmitate) 50000 unit/1 milliliter conventional release solution for injection (clinical drug)| has medicinal product and medicinal product form supertypes with _retinol_ , not _retinol palmitate_. Retinol palmitate is a modification of Retinol and thus should not be used in the creation of the medicinal product and medicinal product form supertypes.

<figure><img src="../../../../../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

Exceptions to use a modified substance are explicitly identified below:

| Exceptions                                               | Elucidation                                                                                                                                             | Examples                                                                                                                                                                                                                                                                                                                                                                                                                    |
| -------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Benzylpenicillin**                                     | When the active ingredient has an _Is modification of_ (attribute) value of 323389000 \|Benzylpenicillin (substance)\|.                                 | 1234765004                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Chemical element compound with multiple modification** | Instances where the chemical element compound has two or more _Is Modification of_ (attribute)s                                                         | 422232005                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Chloral hydrate**                                      | 273948005 \|Chloral hydrate (substance)\| is a modification of Chloral. However, chloral is unstable on its own and always exists in the hydrated form. | 778711000                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Liposome or lipid complex substances**                 | < 414612001                                                                                                                                             | <p>Liposomal agent (substance)</p><p>These subtypes have some sort of modification, but they can be used to create:</p><ul><li>Product containing only x (medicinal product)</li><li>Product containing only x in y dose form (medicinal product form)</li></ul><p>Do not use to create:</p><ul><li>Product containing x (medicinal product)</li><li>Product containing x in y dose form (medicinal product form)</li></ul> |
| **Pegylated substance**                                  | There is no technical way to identify these concepts, though they will often begin with peg-.                                                           | 385544005                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Radiopharmaceutical**                                  | < 89457008 Radioactive isotope (substance)\|                                                                                                            | 783865003                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Silver sulfadiazine**                                  | 387112002 \|Silver sulfadiazine (substance)\| is a modification of 74523009 \|Sulfadiazine (substance)\|.                                               | 864009007                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Sodium valproate**                                     | 387481005 \|Sodium valproate (substance)\| is a modification of 387080000 \|Valproic acid (substance)\|.                                                | 766519009                                                                                                                                                                                                                                                                                                                                                                                                                   |

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Medicinal%20Product%20and%20Medicinal%20Product%20Forms" class="button primary">Provide Feedback</a>
