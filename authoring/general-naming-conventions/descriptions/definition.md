# Definition

A _definition_ is a textual description applied to some SNOMED CT concepts that provides additional information about the intended meaning or usage of the concept. Definitions are not mandated and are considered for addition on a case-by-case basis, and if required, to differentiate a concept from its related concepts.\
Adding a definition to a concept provides additional clarity on its context of use.  It enhances the definition provided by the modeled relationships whereby a term can be sufficiently defined logically, but the words, which is how many look for and interpret meaning, may imply more or less specificity. &#x20;

{% hint style="warning" %}
The definition should never be contradictory to the modeling.
{% endhint %}

Definitions must:

* be written as complete sentences,
* begin with a capital letter,
* end with a period,
* apply a case sensitivity of _Entire term case_ _sensitive_ (CS).

&#x20;

* For example,
  *   The definition for the concept&#x20;

      [11530004 | Brittle diabetes mellitus (finding)|](http://snomed.info/id/11530004) is:&#x20;

      * _Frequent, clinically significant fluctuations in blood glucose levels both above and below levels expected to be achieved by available therapies._

The language acceptability default for a single Definition description is _Preferred._   A definition with varying US and GB English descriptions are each applied with the respective language acceptability. &#x20;

* For example,&#x20;
  * 1332358007 |Full schwannomatosis (disorder)|

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Definition of 1332358007 |Full schwannomatosis (disorder)| with US and GB English acceptability values. </p></figcaption></figure>

### Consideration for text definition <a href="#consideration-for-text-definition" id="consideration-for-text-definition"></a>

A text definition should be considered where a concept references the obscure or unusual.  As an example, _raised blood pressure_ is a commonly used phrase, which, in itself, is ambiguous.  _Raised_ can mean: 1) higher than a previous measurement, 2) on the high side of normal range, or 3) above reference range.  Because of that ambiguity, a full definition created by logical model may be impossible, so a text definition could be used to encourage consistent use of the term. &#x20;

The following principles for definition creation are summarized below from ISO-704, _Terminology work — Principles and methods_:

| Principle               | Explanation                                           |
| ----------------------- | ----------------------------------------------------- |
| **Clarity**             | Avoid ambiguity or overly complex language.           |
| **Conciseness**         | Be as brief as possible without sacrificing meaning.  |
| **Consistency**         | Use a consistent structure and vocabulary.            |
| **Non-circular**        | Do not use the term in the definition.                |
| **Genus + Differentia** | Define by broader category + distinguishing features. |
| **Context-aware**       | Include notes or usage context if necessary.          |

In summary, if a term may be interpreted in multiple ways, but is intended to mean only one way in SNOMED CT, it needs a definition.  However, ultimate source of truth for meaning remains with the FSN.&#x20;

{% hint style="warning" %}
* URLs that point to definition sources are unacceptable.
* External references, such as ISBN and PubMed identifiers, are not allowed in SNOMED CT concept definitions.&#x20;
{% endhint %}

\
