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

These concepts in the International Release, their descriptions, and their `|Has active ingredient (attribute)|` value, represent the **base** ingredient, not a modification.

For example,

`1204319004 |Product containing precisely retinol (as retinol palmitate) 50000 unit/1 milliliter conventional release solution for injection (clinical drug)|` has medicinal product and medicinal product form supertypes with _retinol_ , not _retinol palmitate_. Retinol palmitate is a modification of Retinol and thus should not be used in the creation of the medicinal product and medicinal product form supertypes.

<figure><img src="../../../../../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

Exceptions to use a modified substance are explicitly identified below:

<table><thead><tr><th width="150.32421875">Exceptions</th><th>Elucidation</th><th>Examples</th></tr></thead><tbody><tr><td><strong>Benzylpenicillin</strong></td><td>When the active ingredient has an <em>Is modification of</em> (attribute) value of <code>323389000 |Benzylpenicillin (substance)|</code>.</td><td><p><code>1234765004 |Product containing only benzathine benzylpenicillin in parenteral dose form (medicinal product form)|</code></p><p><br><code>323404007 |Product containing benzathine benzylpenicillin (medicinal product)|</code></p><p><br>Benzylpenicillin is the base, but use the modified substance<br>in the FSN for the MP/MPF.</p></td></tr><tr><td><strong>Chemical element compound with multiple modification</strong></td><td>Instances where the chemical element compound has two or more <em>Is Modification of</em> (attribute)s</td><td><p><code>422232005 |Calcium lactate gluconate (substance)|</code> </p><p>-Has |Is modification of (attribute)| = Calcium gluconate </p><p>-Has |Is modification of (attribute)| = Calcium lactate </p><p></p><p><code>1359973006 |Copper (64-Cu) labeled somatostatin analog (substance)|</code></p><p>-Has |Is modification of (attribute)| = Somatostatin analog </p><p>-Has |Is modification of (attribute)| = Copper-64</p></td></tr><tr><td><strong>Chloral hydrate</strong></td><td><code>273948005 |Chloral hydrate (substance)|</code> is a modification of Chloral. However, chloral is unstable on its own and always exists in the hydrated form.</td><td><p><code>778711000 |Product containing only chloral hydrate in oral dose form (medicinal product form)|</code></p><p><br><code>386735001 |Product containing chloral hydrate in oral dose form (medicinal product form)|</code></p><p><br><code>775158004 |Product containing only chloral hydrate (medicinal product)|</code></p></td></tr><tr><td><strong>Liposome or lipid complex substances</strong></td><td><p><code>&#x3C; 414612001 |Liposomal</code><br><code>agent (substance)</code><br>These subtypes have some sort of modification, but they can be used to create:</p><ul><li>Product containing only x (medicinal product)</li><li>Product containing only x in y dose form (medicinal product form)</li></ul><p>Do not use to create:</p><ul><li>Product containing x (medicinal product)</li><li>Product containing x in y dose form (medicinal product form)</li></ul></td><td><p>426490000 |Vincristine liposome (substance)|</p><p><br>425953004 |Amphotericin B lipid complex (substance)|</p><p><br>768664009 |Amphotericin B phospholipid complex<br>(substance)|</p><p><br>427544000 |Amphotericin B cholesteryl sulfate complex<br>(substance)|</p><p></p></td></tr><tr><td><strong>Pegylated substance</strong></td><td>There is no technical way to identify these concepts, though they will often begin with peg-.</td><td><p>385544005 |Pegfilgrastim (substance)|</p><p><br>770965008 |Pegvaliase (substance)|</p></td></tr><tr><td><strong>Radiopharmaceutical</strong></td><td><code>&#x3C; 89457008 Radioactive isotope (substance)|</code></td><td><p>783865003 |Product containing only cyanocobalamin (58-Co) (medicinal product)|</p><p><br>783867006 |Product containing only cyanocobalamin (58-Co) in oral dose form (medicinal product form)|</p><p><br>783856005 |Product containing sodium iodide (131-I) in parenteral dose form (medicinal product form)|</p><p><br>783854008 |Product containing sodium iodide (131-I) (medicinal product)|</p></td></tr><tr><td><strong>Silver sulfadiazine</strong></td><td><code>387112002 |Silver sulfadiazine</code> <br><code>(substance)|</code> is a modification of <code>74523009 |Sulfadiazine (substance)|</code></td><td><p>864009007 |Product containing only silver sulfadiazine in cutaneous dose form (medicinal product form)|</p><p><br>771756000 |Product containing silver sulfadiazine in cutaneous dose form (medicinal product form)|</p></td></tr><tr><td><strong>Sodium valproate</strong></td><td><code>387481005 |Sodium valproate (substance)|</code> is a modification of <code>387080000 |Valproic acid (substance)|</code>.</td><td><p>766519009 |Product containing precisely sodium valproate 40 milligram/1 milliliter conventional release oral solution (clinical drug)|</p><p><br>1204386001 |Product containing precisely sodium valproate 133 milligram and valproic acid 58 milligram/1 each prolonged-release oral tablet (clinical drug)|</p></td></tr></tbody></table>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Medicinal%20Product%20and%20Medicinal%20Product%20Forms" class="button primary">Provide Feedback</a>
