# Structure of Domain Coverage

SNOMED CT includes 19 _domains_ arranged in a polyhierarchical structure. Each hierarchy is an ordered organization of concepts linked together through _IS A relationships_. Each concept may have one or more parents.

The hierarchical arrangement is helpful for locating concepts, grouping similar concepts, and conveying meaning. For example, if we see the concept _cell_ under the concept _anatomic entity_ we will understand the intended meaning as different than if it appeared under the concepts _room_ or _power source_(Desiderata for Controlled Medical Vocabularies in the Twenty-First Century by J.J. Cimino published in _Methods of_ _Information in Medicine_ 1998:37:394-403).

Concepts are linked to their more general parent concept codes directly above them in a hierarchy. Concepts with more general meanings are usually presented as being at the top of the hierarchy and then at each level down the hierarchy, the meanings become increasingly more specific or specialized.

The domains contain all of the components (clinical, administrative, database structure, as well as other components that express how the domains relate to each other) necessary to create SNOMED CT concepts and maintain the database structure.

| Definition                                                                                                                                                                                                                    | Notes                                                                                                                                     | Examples                                          |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| A domain is a set of concepts that the Concept Model permits to be defined or refined, using a particular set of attributes and ranges. Some domains do not have attributes and ranges, but may if a concept model is created | A domain, to which an attribute can be applied, is typically defined to include concepts in one or more branches of the subtype hierarchy | <p>The domain of</p><p><code>116676008</code></p> |

The following table lists the domains, definitions, and examples. \*Those without a concept model are marked with an asterisk.

\| 1 | Body Structure |

* Anatomical or acquired body structure
* Morphologic abnormality (subtype of body structure)

\


|

* [450807008 | Entire back (body structure)|](http://snomed.info/id/450807008)
* [52988006 | Lesion (morphologic abnormality)|](http://snomed.info/id/52988006)

\| | -- | --------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | | 2 | Clinical Finding |

* Clinical finding: normal/abnormal observations, judgments, or assessments of patients
* Disorder: always and necessarily an abnormal clinical state

|

* [39579001 | Anaphylaxis (disorder)|](http://snomed.info/id/39579001)
* [167222005 | Abnormal urinalysis (finding)|](http://snomed.info/id/167222005)

\| | 3 | Environment and Geographical Location\* |

* Environment: types of environments
* Geographical Location: named locations such as countries, states, or regions

|

* [405607001 | Ambulatory surgery center (environment)|](http://snomed.info/id/405607001)
* [223581004 | China (geographic location)|](http://snomed.info/id/223581004)

\| | 4 | Event |

* Occurrences impacting health or health care; not procedures or interventions

|

* [242039002 | Abuse of partner (event)|](http://snomed.info/id/242039002)
* [2641000119104 | Exposure to chlamydia (event)|](http://snomed.info/id/2641000119104)

\| | 5 | Observable Entity |

* Information about a quality/property to be observed and how it will be observed

|

* [423493009 | Age at diagnosis (observable entity)|](http://snomed.info/id/423493009)
* [416125006 | Concentration of hemoglobin in erythrocyte (observable entity)|](http://snomed.info/id/416125006)

\| | 6 | Organism\* |

* Organisms of significance to human and animal medicine; use in modeling cause of disease

|

* [3265006 | Genus Candida (organism)|](http://snomed.info/id/3265006)
* [710877000 | Beta lactam resistant bacteria (organism)|](http://snomed.info/id/710877000)

\| | 7 | Pharmaceutical/Biological Product |

* Drug products (not Substances)

|

* [400687000 | Infliximab 100mg/vial powder for reconstitution injection (product)|](http://snomed.info/id/400687000)
* [317222006 | Product containing only cimetidine 200 mg/1 each oral tablet (clinical drug)|](http://snomed.info/id/317222006)

\| | 8 | Physical Force\* |

* Forces applied to the body that may cause injury

|

* [57955009 | Hot weather (physical force)|](http://snomed.info/id/57955009)
* [285719001 | Mechanical abrasion (physical force)|](http://snomed.info/id/285719001)

\| | 9 | Physical Object\* |

* Physical devices relevant to health care, or to injuries/accidents

|

* [15237007 | Sitz bath chair, device (physical object)|](http://snomed.info/id/15237007)
* [69861004 | Firearm, device (physical object)|](http://snomed.info/id/69861004)

\| | 10 | Procedure |

* Procedure: activities performed in the provision of health care (includes medical history-taking, physical examination, diagnostic and therapeutic interventions, training and education, and counseling)
* Regime/therapy (subtype of procedure): set of procedures focused on a single purpose on one patient over time (e.g. repeated administration of drug in a small dose for an indefinite period of time)

|

* [54321008 | Cardiac flow imaging (procedure)|](http://snomed.info/id/54321008)
* [386513007 | Anesthesia management (regime/therapy)|](http://snomed.info/id/386513007)

\| | 11 | Qualifier Value\* |

* One of several possible values for an attribute used to define concepts

|

* [90734009 | Chronic (qualifier value)|](http://snomed.info/id/90734009)
* [255412001 | Appearances (qualifier value)|](http://snomed.info/id/255412001)

\| | 12 | Record Artifact\* |

* Clinical documents, or parts thereof

|

* [445673000 | Original report (record artifact)|](http://snomed.info/id/445673000)
* [41000179103 | Immunization record (record artifact)|](http://snomed.info/id/41000179103)

\| | 13 | Situation with Explicit Context |

* Concepts that include context information; a subtype of the situation to which it applies with an attribute associating it with the relevant clinical finding or procedure
* May be used to represent conditions/procedures that already occurred, haven't yet occurred, or refer to someone else (not patients)

|

* [169589005 | Antenatal care: history of infertility (situation)|](http://snomed.info/id/169589005)
* [407565004 | Angiotensin II receptor antagonist not tolerated (situation)|](http://snomed.info/id/407565004)

\| | 14 | SNOMED CT Model Component\* |

* Concepts and attributes necessary to organize and structure SNOMED CT terminology and its derivatives

|

* [900000000000442005 | Core metadata concept (core metadata concept)|](http://snomed.info/id/900000000000442005)
* [900000000000454005 | Foundation metadata concept (foundation metadata concept)|](http://snomed.info/id/900000000000454005)
* [106237007 | Linkage concept (linkage concept)|](http://snomed.info/id/106237007)
* [370136006 | Namespace concept (namespace concept)|](http://snomed.info/id/370136006)

\| | 15 | Social Context\* |

* Social conditions and circumstances related to healthcare
* Subtypes include: ethnic group, life style, occupation, person, racial group, religion/philosophy, s ocial concept

|

* [116060000 | Eating habit (life style)|](http://snomed.info/id/116060000)
* [58626002 | Legal guardian (person)|](http://snomed.info/id/58626002)
* [415794004 | Unknown racial group (racial group)|](http://snomed.info/id/415794004)
* [35359004 | Family (social concept)|](http://snomed.info/id/35359004)

\| | 16 | Special Concept\* |

* Inactive and navigational (support locating concepts in hierarchies) concept codes

|

* [363664003 | Erroneous concept (inactive concept)|](http://snomed.info/id/363664003)
* [394899003 | Oral administration of treatment (navigational concept)|](http://snomed.info/id/394899003)

\| | 17 | Specimen |

* Entities that are obtained (usually from patients) for examination or analysis

|

* [373193000 | Lymph node from sentinel lymph node dissection (specimen)|](http://snomed.info/id/373193000)
* [258441009 | Exudate sample (specimen)|](http://snomed.info/id/258441009)

\| | 18 | Staging and Scales\* |

* Assessment and tumor staging scales

|

* [273472005 | Functional status index (assessment scale)|](http://snomed.info/id/273472005)
* [254294008 | Tumor-node-metastasis (TNM) head and neck tumor staging (tumor staging)|](http://snomed.info/id/254294008)

\| | 19 | Substance |

* Active chemical constituents of allergens, agents, substances, chemicals, drugs, and materials (not Pharmaceutical/Biological Products)

|

* [116272000 | Dietary fiber (substance)|](http://snomed.info/id/116272000)
* [64856004 | Digestive system fluid (substance)|](http://snomed.info/id/64856004)

|

## Granularity

The scale, or level of detail, in a terminology is called _granularity_. Concepts and meanings range from very general, or coarse, to very specific, or fine. SNOMED CT has multiple granularities, which is an important component of terminologies that are multipurpose. The broader meanings are useful for aggregation (e.g. Clinical finding, Procedure, etc.), but are not intended for recording individual patient data.

The progressive levels of refinement are used to meet clinical data requirements. There are, however, limits to the degree of precoordination of certain types of complex statements.

In general, concepts in SNOMED CT should name things that exist in the real world. The concepts are usually names or short noun phrases, not complete sentences or paragraphs.

SNOMED CT is intended to be used with electronic health applications that can support full clinical statements, along with their attributions, dates, times, and statement interrelationships. It may be challenging to balance SNOMED CT content with the needs of those using electronic health applications. For example, some older applications may require concepts outside of the scope of SNOMED CT. SNOMED CT tries to maximize its usefulness and at the same time minimize precoordination.
