# Proximal Primitive Modeling

See glossary for definition here:

* [proximal primitive parent](https://app.gitbook.com/s/P21QucCX9Y41nBQt50ad/p/proximal-primitive-parent "mention")
* [proximal primitive supertype](https://app.gitbook.com/s/P21QucCX9Y41nBQt50ad/p/proximal-primitive-supertype "mention")

***

* For some, but not all concepts, the proximal primitive parent is a top level concept, e.g., Procedure.
* The proximal primitive supertype may also be an intermediate primitive concept located between the top level concept and the concept in question.
* There may be more than one proximal primitive supertype for a concept.

The approved modeling approach is to use:

* Proximal primitive supertypes
* Attribute-value pairs sufficient to define the meaning
  * An attribute-value pair is explicitly stated for the concept, even if it is already present for a supertype concept.
  * Attribute-value pairs are grouped as required.

The classifier infers all appropriate proximal supertypes. With sufficiently defined concepts the subtypes are also inferred.

* For example,
  *   The proximal primitive supertype for this concept is

      [71388002 | Procedure (procedure)|](http://snomed.info/id/71388002). It has been modeled with one stated supertype and two attribute value pairs in a relationship group.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Stated view of<a href="http://snomed.info/id/702499000">702499000 | Computed tomography of humerus (procedure)|</a></p></figcaption></figure>

The _inferred_ view shows the logical definition of the concept. By using the stated relationships (for this concept and other concepts currently in the terminology), the classifier infers three defined proximal supertypes:

* Radiography of humerus (procedure)
* Computed tomography of upper arm (procedure)
* Computed tomography of bone (procedure)

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Inferred view of <a href="http://snomed.info/id/702499000">702499000 | Computed tomography of humerus (procedure)|</a></p></figcaption></figure>

### Multiple potential primitive supertype concepts <a href="#multiple-potential-primitive-supertype-concepts" id="multiple-potential-primitive-supertype-concepts"></a>

Where more than one potential primitive supertype is identified for a concept, authors should check the primitive supertypes for subsumption of one or more other primitive supertypes. Any subsuming concept is not a proximal primitive supertype.

* For example,
  *   There is more than one potential primitive supertype for

      [421095001 | Allergic disorder by body site affected (disorder)|](http://snomed.info/id/421095001). However, [64572001 | Disease (disorder)|](http://snomed.info/id/64572001) is subsumed by [404684003 | Clinical finding (finding)|](http://snomed.info/id/404684003), therefore[64572001 | Disease (disorder)|](http://snomed.info/id/64572001)is the proximal primitive supertype concept.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### GCI-Modeled primitive supertypes <a href="#gci-modeled-primitive-supertypes" id="gci-modeled-primitive-supertypes"></a>

For information on the effect of GCIs on modeling primitive supertypes, see [General Concept Inclusions (GCIs), GCI-Modeled Primitive Ancestor](https://conf.spaces.snomed.org/wiki/spaces/DOCEG/pages/133244597).

\\
