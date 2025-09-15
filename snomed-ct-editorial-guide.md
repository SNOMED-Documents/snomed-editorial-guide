# SNOMED CT Editorial Guide

<figure><img src="attachments/27591252/35987732.png" alt="" title=""><figcaption><p><em><strong>These guidelines should be applied to new content. While there are many concepts in the existing content that are not in compliance with this guidance, the process of correcting existing content will be carried out as time and resources permit.</strong></em></p></figcaption></figure>

  

The Editorial Guide provides the information necessary to model concepts in SNOMED CT. It is a working document, subject to change and revision. The primary audience is for those who edit content in the International Release _,_ but it may also be useful to those creating extensions. For those editing in extensions, please also see guidance within the [Extensions Practical Guide](https://docs.snomed.org/snomed-ct-practical-guides/snomed-ct-extension-guide/). 

SNOMED CT is distributed in sets of electronic files. Supporting software tools are not necessarily provided directly by SNOMED International.

Welcome to <http://snomed.org/eg>

[Video introduction to the Editorial Guide](https://drive.google.com/file/d/1OuQixcCCM1N-BuKxTH6LDfvggTB1NJM7/view?usp=sharing)

[Summary of changes](https://docs.google.com/spreadsheets/d/1xHZNeNQwkCcUPaZGEl28GFGv_WMTHZoeHeAV5cSjOFU/)*

*_Changes on this spreadsheet may include those in progress for a future publication date. The in-progress changes are available for viewing but will not be visible in the Editorial Guide until the next publication. Please note dates in bottom tab._

The Editorial Guide publishes only the rules that apply to precoordinated content. That is, the rules where the 'Content Type' is one of the following - |All SNOMED CT content|, |All precoordinated SNOMED CT content|, or |All new precoordinated SNOMED CT content|. The rules that are **not** published in the Editorial Guide are the ones that apply only to |All postcoordinated content|. See the different content types and rules in the MRCM maintenance tool at <https://browser.ihtsdotools.org/mrcm>. 

Text that is protected by copyright will not be accepted for inclusion unless accompanied by a release from the copyright holder.

| © Copyright 2025International Health Terminology Standards Development Organisation, all rights reserved.This document is a publication of International Health Terminology Standards Development Organisation, trading as SNOMED International. SNOMED International owns and maintains SNOMED CT®.Any modification of this document (including without limitation the removal or modification of this notice) is prohibited without the express written permission of SNOMED International. This document may be subject to updates. Always use the latest version of this document published by SNOMED International. This can be viewed online and downloaded by following the links on the front page or cover of this document.SNOMED®, SNOMED CT® and IHTSDO® are registered trademarks of International Health Terminology Standards Development Organisation. SNOMED CT® licensing information is available athttp://snomed.org/licensing. For more information about SNOMED International and SNOMED International Membership, please refer tohttp://www.snomed.orgor contact us atinfo@snomed.org. |
|---|

**Contents  
**

#### [SNOMED CT Introduction](SNOMED-CT-Introduction_174690273.html)

  * [Intended Use](Intended-Use_174690274.html)
  * [Structure of Domain Coverage](Structure-of-Domain-Coverage_174690276.html)
  * [Knowledge Representation](Knowledge-Representation_174690277.html)
  * [Out of Scope](Out-of-Scope_174690275.html)
  * [SNOMED CT Requirements](SNOMED-CT-Requirements_174690278.html)
    * [Medical Vocabularies - J. Cimino](Medical-Vocabularies---J.-Cimino_174690279.html)
    * [Electronic Health Applications](Electronic-Health-Applications_174690280.html)
    * [Implementation and Migration](Implementation-and-Migration_174690281.html)
    * [User Communities](User-Communities_174690282.html)
    * [Summary of SNOMED CT Requirements](Summary-of-SNOMED-CT-Requirements_174690283.html)

#### [Concept Model Overview](Concept-Model-Overview_174691757.html)

  * [Root and Top-level Concepts](Root-and-Top-level-Concepts_174691758.html)
  * [Attributes](Attributes_174691762.html)
  * [Defining Characteristics](Defining-Characteristics_174691761.html)
  * [Qualifying Characteristics](Qualifying-Characteristics_174691763.html)

#### [Authoring](Authoring_174690284.html)

  * [Scope](Scope_174690285.html)
    * [Adjudication for Content Requests](Adjudication-for-Content-Requests_174690288.html)
    * [Proprietary Names and Works](Proprietary-Names-and-Works_174690286.html)
  * [General Naming Conventions](General-Naming-Conventions_174691646.html)
    * [Descriptions](Descriptions_174691647.html)
    * [Case Significance](Case-Significance_174691658.html)
    * [Person Naming Conventions](Person-Naming-Conventions_174691660.html)
    * [Plurals](Plurals_174691661.html)
    * [Punctuation and Symbols](Punctuation-and-Symbols_174691662.html)
    * [Sentence Types](Sentence-Types_174691663.html)
    * [US vs. GB English](US-vs.-GB-English_174691664.html)
    * [Action Verbs](Action-Verbs_174691666.html)
    * [Numbers and Numeric Ranges](Numbers-and-Numeric-Ranges_174691667.html)
  * [General Modeling](General-Modeling_174691668.html)
    * [Annotations](Annotations_256869349.html)
    * [Changes to Components](Changes-to-Components_174691723.html)
    * [Conjunction and Disjunction](Conjunction-and-Disjunction_174691733.html)
    * [General Concept Inclusions - GCIs](General-Concept-Inclusions---GCIs_174691736.html)
    * [Grouper Concept](Grouper-Concept_174691686.html)
    * [Intermediate Primitive Concept Modeling](Intermediate-Primitive-Concept-Modeling_174691685.html)
    * [Proximal Primitive Modeling](Proximal-Primitive-Modeling_174691676.html)
    * [Relationship Group](Relationship-Group_174691688.html)
    * [Sufficiently Defined vs Primitive Concept](Sufficiently-Defined-vs-Primitive-Concept_174691669.html)
    * [Templates](Templates_174691756.html)
  * [Domain Specific Modeling](Domain-Specific-Modeling_174690289.html)
    * [Body Structure](Body-Structure_174690290.html)
    * [Clinical Finding and Disorder](Clinical-Finding-and-Disorder_174690335.html)
    * [Environment and Geographical Location](Environment-and-Geographical-Location_174690590.html)
    * [Event](Event_174690591.html)
    * [Observable Entity](Observable-Entity_174690597.html)
    * [Organism](Organism_174690618.html)
    * [Pharmaceutical and Biologic Product](Pharmaceutical-and-Biologic-Product_174690621.html)
    * [Physical Force](Physical-Force_174691256.html)
    * [Physical Object](Physical-Object_174691257.html)
    * [Procedure](Procedure_174691281.html)
    * [Qualifier Value](Qualifier-Value_174691360.html)
    * [Record Artifact](Record-Artifact_174691379.html)
    * [Situation with Explicit Context](Situation-with-Explicit-Context_174691381.html)
    * [SNOMED CT Model Component](SNOMED-CT-Model-Component_174691387.html)
    * [Social Context](Social-Context_174691391.html)
    * [Special Concept](Special-Concept_174691392.html)
    * [Specimen](Specimen_174691394.html)
    * [Staging and Scales](Staging-and-Scales_174691397.html)
    * [Substance](Substance_174691398.html)

#### [Editorial Guide Style and Terms](Editorial-Guide-Style-and-Terms_174691764.html)

#### [PDFs for Download](PDFs-for-Download_174691765.html)
