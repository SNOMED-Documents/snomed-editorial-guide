# SNOMED CT Editorial Guide

This Editorial Guide is used for Education Purposes Only. It is used in the Authoring Courses and Certifications. It is based on the January 2025 Editorial Guide.

<figure><img src="attachments/27591252/35987732.png" alt="" title=""><figcaption><p><em><strong>These guidelines should be applied to new content. While there are many concepts in the existing content that are not in compliance with this guidance, the process of correcting existing content will be carried out as time and resources permit.</strong></em></p></figcaption></figure>

  

The Editorial Guide provides the information necessary to model concepts in SNOMED CT. It is a working document, subject to change and revision. The primary audience is for those who edit content in the International Release _,_ but it may also be useful to those creating extensions. For those editing in extensions, please also see guidance within the [Extensions Practical Guide](https://confluence.ihtsdotools.org/display/DOCEXTPG/Extensions+Practical+Guide). 

SNOMED CT is distributed in sets of electronic files. Supporting software tools are not necessarily provided directly by SNOMED International.

Welcome to

| Education version of Editorial Guide http://snomed.org/EDEG |
|---|

  

[Video introduction to the Editorial Guide](https://drive.google.com/file/d/1OuQixcCCM1N-BuKxTH6LDfvggTB1NJM7/view?usp=sharing)

The Editorial Guide publishes only the rules that apply to precoordinated content. That is, the rules where the 'Content Type' is one of the following - |All SNOMED CT content|, |All precoordinated SNOMED CT content|, or |All new precoordinated SNOMED CT content|. The rules that are **not** published in the Editorial Guide are the ones that apply only to |All postcoordinated content|. See the different content types and rules in the MRCM maintenance tool at <https://browser.ihtsdotools.org/mrcm>. 

Text that is protected by copyright will not be accepted for inclusion unless accompanied by a release from the copyright holder.

| © Copyright 2025International Health Terminology Standards Development Organisation, all rights reserved.This document is a publication of International Health Terminology Standards Development Organisation, trading as SNOMED International. SNOMED International owns and maintains SNOMED CT®.Any modification of this document (including without limitation the removal or modification of this notice) is prohibited without the express written permission of SNOMED International. This document may be subject to updates. Always use the latest version of this document published by SNOMED International. This can be viewed online and downloaded by following the links on the front page or cover of this document.SNOMED®, SNOMED CT® and IHTSDO® are registered trademarks of International Health Terminology Standards Development Organisation. SNOMED CT® licensing information is available athttp://snomed.org/licensing. For more information about SNOMED International and SNOMED International Membership, please refer tohttp://www.snomed.orgor contact us atinfo@snomed.org. |
|---|

**Contents  
**

#### [SNOMED CT Introduction](SNOMED-CT-Introduction_179930657.html)

  * [Intended Use](Intended-Use_179930658.html)
  * [Structure of Domain Coverage](Structure-of-Domain-Coverage_179930660.html)
  * [Knowledge Representation](Knowledge-Representation_179930661.html)
  * [Out of Scope](Out-of-Scope_179930659.html)
  * [SNOMED CT Requirements](SNOMED-CT-Requirements_179930662.html)
    * [Medical Vocabularies - J. Cimino](Medical-Vocabularies---J.-Cimino_179930663.html)
    * [Electronic Health Applications](Electronic-Health-Applications_179930664.html)
    * [Implementation and Migration](Implementation-and-Migration_179930665.html)
    * [User Communities](User-Communities_179930666.html)
    * [Summary of SNOMED CT Requirements](Summary-of-SNOMED-CT-Requirements_179930667.html)

#### [Concept Model Overview](Concept-Model-Overview_179932141.html)

  * [Root and Top-level Concepts](Root-and-Top-level-Concepts_179932142.html)
  * [Attributes](Attributes_179932146.html)
  * [Defining Characteristics](Defining-Characteristics_179932145.html)
  * [Qualifying Characteristics](Qualifying-Characteristics_179932147.html)

#### [Authoring](Authoring_179930668.html)

  * [Scope](Scope_179930669.html)
    * [Adjudication for Content Requests](Adjudication-for-Content-Requests_179930672.html)
    * [Proprietary Names and Works](Proprietary-Names-and-Works_179930670.html)
  * [General Naming Conventions](General-Naming-Conventions_179932030.html)
    * [Descriptions](Descriptions_179932031.html)
    * [Case Significance](Case-Significance_179932042.html)
    * [Person Naming Conventions](Person-Naming-Conventions_179932044.html)
    * [Plurals](Plurals_179932045.html)
    * [Punctuation and Symbols](Punctuation-and-Symbols_179932046.html)
    * [Sentence Types](Sentence-Types_179932047.html)
    * [US vs. GB English](US-vs.-GB-English_179932048.html)
    * [Action Verbs](Action-Verbs_179932050.html)
    * [Numbers and Numeric Ranges](Numbers-and-Numeric-Ranges_179932051.html)
  * [General Modeling](General-Modeling_179932052.html)
    * [Annotations](Annotations_273518997.html)
    * [Changes to Components](Changes-to-Components_179932107.html)
    * [Conjunction and Disjunction](Conjunction-and-Disjunction_179932117.html)
    * [General Concept Inclusions - GCIs](General-Concept-Inclusions---GCIs_179932120.html)
    * [Grouper Concept](Grouper-Concept_179932070.html)
    * [Intermediate Primitive Concept Modeling](Intermediate-Primitive-Concept-Modeling_179932069.html)
    * [Proximal Primitive Modeling](Proximal-Primitive-Modeling_179932060.html)
    * [Relationship Group](Relationship-Group_179932072.html)
    * [Sufficiently Defined vs Primitive Concept](Sufficiently-Defined-vs-Primitive-Concept_179932053.html)
    * [Templates](Templates_179932140.html)
  * [Domain Specific Modeling](Domain-Specific-Modeling_179930673.html)
    * [Body Structure](Body-Structure_179930674.html)
    * [Clinical Finding and Disorder](Clinical-Finding-and-Disorder_179930719.html)
    * [Environment and Geographical Location](Environment-and-Geographical-Location_179930976.html)
    * [Event](Event_179930977.html)
    * [Observable Entity](Observable-Entity_179930983.html)
    * [Organism](Organism_179931004.html)
    * [Pharmaceutical and Biologic Product](Pharmaceutical-and-Biologic-Product_179931007.html)
    * [Physical Force](Physical-Force_179931641.html)
    * [Physical Object](Physical-Object_179931642.html)
    * [Procedure](Procedure_179931666.html)
    * [Qualifier Value](Qualifier-Value_179931745.html)
    * [Record Artifact](Record-Artifact_179931764.html)
    * [Situation with Explicit Context](Situation-with-Explicit-Context_179931765.html)
    * [SNOMED CT Model Component](SNOMED-CT-Model-Component_179931771.html)
    * [Social Context](Social-Context_179931775.html)
    * [Special Concept](Special-Concept_179931776.html)
    * [Specimen](Specimen_179931778.html)
    * [Staging and Scales](Staging-and-Scales_179931781.html)
    * [Substance](Substance_179931782.html)

#### [Editorial Guide Style and Terms](Editorial-Guide-Style-and-Terms_179932148.html)

#### [PDFs for Download](PDFs-for-Download_179932149.html)
