# Knowledge Representation

Knowledge representation in SNOMED CT involves modeling what we know about concepts to be necessarily true. Concepts are logically defined by their relationships to each other. Some knowledge provides valuable clues to the diagnostician, while not necessarily always present, i.e. it is uncertain or probabilistic knowledge. Attempts to capture probabilistic or uncertain knowledge are out of the scope of SNOMED CT.

{% code title="Example Concept" overflow="wrap" %}
```
22298006 | Myocardial infarction (disorder)|
```
{% endcode %}

Its terminological knowledge includes the following:

{% code title="Concept Properties" %}
```
IS A: 
64572001 | Disease (disorder)|

Finding site: 
74281007 | Myocardium structure (body structure)|

Associated morphology: 
55641003 | Infarct (morphologic abnormality)|
```
{% endcode %}

_These additional pieces of knowledge are variably present and therefore represent uncertain or probabilistic knowledge about myocardial infarction:_

* Crushing substernal chest pain
* Diaphoresis
* Arrhythmia
* ST-segment elevation on EKG
* Elevated cardiac enzymes

Another example:

{% code title="Example Concept" overflow="wrap" %}
```
74400008 | Appendicitis (disorder)|
```
{% endcode %}

Its terminological knowledge includes the following:

{% code title="Concept Properties" %}
```
IS A: 
64572001 | Disease (disorder)|

Finding site: 
66754008 | Appendix structure (body structure)|

Associated morphology: 
23583003 | Inflammation (morphologic abnormality)|
```
{% endcode %}

_These additional pieces of knowledge are variably present and therefore represent uncertain or probabilistic knowledge about appendicitis:_

* Central abdominal pain that migrates to the right lower quadrant
* Rebound tenderness over McBurneys point
* Anorexia
* Nausea
* Elevated white blood count






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=SCT+Editorial+Guide&entry.670899847=Knowledge%20Representation" class="button primary">Provide Feedback</a>
