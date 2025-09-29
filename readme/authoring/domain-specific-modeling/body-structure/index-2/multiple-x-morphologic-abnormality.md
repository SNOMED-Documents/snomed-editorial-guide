# Multiple x morphologic abnormality

_Multiple x_ morphologies, such as 125291005 |Multiple cysts (morphologic abnormality)|, are currently subtypes of the “X” morphology. The “X” morphology concept represents a class rather than a singular instance, and this arrangement follows the open world assumption of the description logic in SNOMED CT.

* For example,
  * _Cyst of upper eyelid_ does not mean a single cyst on a single upper eyelid. It represents a class of cyst condition that at least appeared in an upper eyelid. This class would also include a cyst condition involving both upper and lower eyelids.
  * A similar example is how |Retinitis of bilateral eyes (disorder)| is a subconcept of |Retinitis of left eye (disorder)| and |Retinitis of right eye (disorder)|.

Having the _Multiple X_ morphologic abnormality concept as a subtype of the “X” morphology concept allows the disorder concepts defined by these “multiple X” morphologies to be sufficiently defined. One drawback of the current format is that classification results are not complete.

* For example,
  * _Multiple cysts of eyelid_ would not subsume _cysts of upper and lower eyelids_ in the current concept model.

{% hint style="warning" %}
In the future, these disorder concepts may be updated with a more robust representation utilizing cardinality as part of the logical definition. However, this functionality is not available in the reasoner profile of SNOMED CT at this time.
{% endhint %}

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Multiple%20x%20morphologic%20abnormality" class="button primary">Provide Feedback</a>
