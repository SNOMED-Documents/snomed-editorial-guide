# Synonym

In SNOMED CT, a  _synonym (SYN)_ is a description that is an acceptable way to express the meaning of a concept in a particular language or dialect, i.e. it is a word or phrase, other than the FSN, that represents a concept. Unlike FSNs, synonyms are not required to be unique. 

Each concept may have one or more synonyms. 

For example,

  *     * US English synonyms for [ 22298006 | Myocardial infarction (disorder)|](http://snomed.info/id/22298006 "22298006 | Myocardial infarction \(disorder\) |") are: 
      * Myocardial infarction
      * Cardiac infarction
      * Heart attack
      * Infarction of heart
      * MI - myocardial infarction
      * Myocardial infarct

A synonym may not change to, i.e. replace, an existing FSN.

## Duplicate terms as synonyms

In most cases, it is unacceptable to add the same term as a synonym to more than one concept. However, some terms have more than one meaning and can be synonyms for more than one concept.   

When concepts have the same term as synonyms, they are checked to determine whether or not they are duplicates. If they are duplicates, one concept is inactivated with a historical association link of SAME_AS to the other concept.

A synonym with a single meaning may be erroneously associated with more than one concept. If the concepts are not duplicates, the synonym should be retained with only one of the concepts and inactivated on the others.

Although uncommon, a term may be acceptable as a synonym for two or more concepts. This depends on the context.

For example,

  *     * _Blister_ in the context of a drug administration unit vs a skin disorder

## Narrower synonym

When a synonym is more specific than the FSN, it does not have the same meaning, and should be inactivated. The description inactivation value of 723278000 |Not semantically equivalent component (foundation metadata concept)| is used.

For example: 

  *     * FSN: Removal of device (procedure)
    * SYN: Replacement of prosthetic device (procedure) - more specific meaning than the FSN

## Broader synonym

When a synonym is more general than the FSN, and there is no context in which it has the same meaning as the FSN, the synonym should be inactivated. The description inactivation value of 723278000 |Not semantically equivalent component (foundation metadata concept)| is used.

For example, 

  *     * FSN: Sprain (morphologic abnormality)
    * SYN: Joint injury - more general meaning than the FSN

However, a more general synonym is acceptable when there is a context in which the synonym has the same meaning as the FSN.

For example:

  *     * FSN: Entire fundus uteri (body structure)
    * SYN: Fundus in the context of obstetrics - same meaning as the FSN

