---
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: false
  tags:
    visible: true
  actions:
    visible: true
  anchors:
    visible: true
---

# Pharmaceutical and Biologic Product and Dose Form Attributes Summary

When authoring in this domain, these are the approved attributes and allowable ranges.

See also respective [Templates](https://conf.spaces.snomed.org/wiki/spaces/SCTEMPLATES/pages/133993757/Product+templates).

## Domain Information for Pharmaceutical/Biologic Product

| Property                      | Value                                                          |
| ----------------------------- | -------------------------------------------------------------- |
| Domain Constraint             | << 373873005 \| Pharmaceutical / biologic product (product) \| |
| Parent Domain                 | -                                                              |
| Proximal Primitive Constraint | << 373873005 \| Pharmaceutical / biologic product (product) \| |
| Proximal Primitive Refinement | -                                                              |

#### Author View of Attributes and Ranges for Pharmaceutical/Biologic Product

| Attribute                                                                 | Grouped | Cardinality | In Group Cardinality | Range Constraint                                                     |
| ------------------------------------------------------------------------- | ------- | ----------- | -------------------- | -------------------------------------------------------------------- |
| 1142140007 \| Count of active ingredient (attribute) \|                   | 0       | 0..1        | 0..0                 | int(>#0..)                                                           |
| 1142141006 \| Count of base and modification pair (attribute) \|          | 0       | 0..1        | 0..0                 | int(>#0..)                                                           |
| 1142139005 \| Count of base of active ingredient (attribute) \|           | 0       | 0..1        | 0..0                 | int(>#0..)                                                           |
| 127489000 \| Has active ingredient (attribute) \|                         | 1       | 0..\*       | 0..1                 | << 105590001 \| Substance (substance) \|                             |
| 732943007 \| Has basis of strength substance (attribute) \|               | 1       | 0..\*       | 0..1                 | < 105590001 \| Substance (substance) \|                              |
| 733722007 \| Has concentration strength denominator unit (attribute) \|   | 1       | 0..\*       | 0..1                 | < 767524001 \| Unit of measure (qualifier value) \|                  |
| 1142137007 \| Has concentration strength denominator value (attribute) \| | 1       | 0..\*       | 0..1                 | dec(>#0..)                                                           |
| 733725009 \| Has concentration strength numerator unit (attribute) \|     | 1       | 0..\*       | 0..1                 | < 767524001 \| Unit of measure (qualifier value) \|                  |
| 1142138002 \| Has concentration strength numerator value (attribute) \|   | 1       | 0..\*       | 0..1                 | dec(>#0..)                                                           |
| 762951001 \| Has ingredient (attribute) \|                                | 1       | 0..\*       | 0..1                 | << 105590001 \| Substance (substance) \|                             |
| 860779006 \| Has ingredient characteristic (attribute) \|                 | 1       | 0..\*       | 0..\*                | << 362981000 \| Qualifier value (qualifier value) \|                 |
| 1149366004 \| Has ingredient qualitative strength (attribute) \|          | 1       | 0..\*       | 0..1                 | < 1149484003 \| Ingredient qualitative strength (qualifier value) \| |
| 411116001 \| Has manufactured dose form (attribute) \|                    | 0       | 0..1        | 0..0                 | << 736542009 \| Pharmaceutical dose form (dose form) \|              |
| 762949000 \| Has precise active ingredient (attribute) \|                 | 1       | 0..\*       | 0..1                 | << 105590001 \| Substance (substance) \|                             |
| 732947008 \| Has presentation strength denominator unit (attribute) \|    | 1       | 0..\*       | 0..1                 | < 767524001 \| Unit of measure (qualifier value) \|                  |
| 1142136003 \| Has presentation strength denominator value (attribute) \|  | 1       | 0..\*       | 0..1                 | dec(>#0..)                                                           |
| 732945000 \| Has presentation strength numerator unit (attribute) \|      | 1       | 0..\*       | 0..1                 | < 767524001 \| Unit of measure (qualifier value) \|                  |
| 1142135004 \| Has presentation strength numerator value (attribute) \|    | 1       | 0..\*       | 0..1                 | dec(>#0..)                                                           |
| 860781008 \| Has product characteristic (attribute) \|                    | 0       | 0..\*       | 0..0                 | << 362981000 \| Qualifier value (qualifier value) \|                 |
| 774158006 \| Has product name (attribute) \|                              | 0       | 0..1        | 0..0                 | << 774167006 \| Product name (product name) \|                       |
| 774159003 \| Has supplier (attribute) \|                                  | 0       | 0..1        | 0..0                 | << 774164004 \| Supplier (supplier) \|                               |
| 1149367008 \| Has target population (attribute) \|                        | 0       | 0..1        | 0..0                 | < 27821000087106 \| Product target population (qualifier value) \|   |
| 763032000 \| Has unit of presentation (attribute) \|                      | 0       | 0..1        | 0..0                 | << 732935002 \| Unit of presentation (unit of presentation) \|       |
| 766939001 \| Plays role (attribute) \|                                    | 0       | 0..\*       | 0..0                 | << 766940004 \| Role (role) \|                                       |
| 1148793005 \| Unit of presentation size quantity (attribute) \|           | 0       | 0..1        | 0..0                 | dec(>#0..)                                                           |
| 320091000221107 \| Unit of presentation size unit (attribute) \|          | 0       | 0..1        | 0..0                 | << 767524001 \| Unit of measure (qualifier value) \|                 |

## Domain Information for Medicinal Product Package

| Property                      | Value                                                       |
| ----------------------------- | ----------------------------------------------------------- |
| Domain Constraint             | << 781405001 \| Medicinal product package (product) \|      |
| Parent Domain                 | 373873005 \| Pharmaceutical / biologic product (product) \| |
| Proximal Primitive Constraint | << 781405001 \| Medicinal product package (product) \|      |
| Proximal Primitive Refinement | -                                                           |

#### Author View of Attributes and Ranges for Medicinal Product Package

<table><thead><tr><th width="203.29693603515625">Attribute</th><th width="108.8436279296875">Grouped</th><th width="101.7291259765625">Cardinality</th><th width="111.2552490234375">In Group Cardinality</th><th>Range Constraint</th></tr></thead><tbody><tr><td>774160008 | Contains clinical drug (attribute) |</td><td>1</td><td>1..*</td><td>1..1</td><td>&#x3C;&#x3C; 763158003 | Medicinal product (product) |</td></tr><tr><td>1142143009 | Count of clinical drug type (attribute) |</td><td>0</td><td>1..1</td><td>0..0</td><td>int(>#0..)</td></tr><tr><td>30465011000036106 |Has container type (attribute)|</td><td>0</td><td>0..1</td><td>0..0</td><td>49062001 |Device (physical object)|</td></tr><tr><td>1142142004 | Has pack size (attribute) |</td><td>1</td><td>0..*</td><td>0..1</td><td>dec(>#0..)</td></tr><tr><td>774163005 | Has pack size unit (attribute) |</td><td>1</td><td>0..*</td><td>0..1</td><td>&#x3C;&#x3C; 767524001 | Unit of measure (qualifier value) |</td></tr></tbody></table>

## Domain Information for Pharmaceutical Dose Form

<table><thead><tr><th width="305.4114990234375">Property</th><th>Value</th></tr></thead><tbody><tr><td>Domain Constraint</td><td>&#x3C;&#x3C; 736542009 | Pharmaceutical dose form (dose form) |</td></tr><tr><td>Parent Domain</td><td>-</td></tr><tr><td>Proximal Primitive Constraint</td><td>&#x3C;&#x3C; 736542009 | Pharmaceutical dose form (dose form) |</td></tr><tr><td>Proximal Primitive Refinement</td><td>-</td></tr></tbody></table>

#### Author View of Attributes and Ranges for Pharmaceutical Dose Form

<table><thead><tr><th width="216.9869384765625">Attribute</th><th width="92.449951171875">Grouped</th><th width="95.422607421875">Cardinality</th><th width="96.451171875">In Group Cardinality</th><th>Range Constraint</th></tr></thead><tbody><tr><td>736476002 | Has basic dose form (attribute) |</td><td>0</td><td>0..1</td><td>0..0</td><td>&#x3C; 736478001 | Basic dose form (basic dose form) |</td></tr><tr><td>736472000 | Has dose form administration method (attribute) |</td><td>0</td><td>0..*</td><td>0..0</td><td>&#x3C; 736665006 | Dose form administration method (administration method) |</td></tr><tr><td>1402355005 |Has dose form after transformation (attribute)|</td><td>0</td><td>0..1</td><td>0..0</td><td>&#x3C; 736542009 |Pharmaceutical dose form (dose form)|</td></tr><tr><td>736474004 | Has dose form intended site (attribute) |</td><td>0</td><td>0..*</td><td>0..0</td><td>&#x3C; 736479009 | Dose form intended site (intended site) |</td></tr><tr><td>736475003 | Has dose form release characteristic (attribute) |</td><td>0</td><td>0..1</td><td>0..0</td><td>&#x3C; 736480007 | Dose form release characteristic (release characteristic) |</td></tr><tr><td>736473005 | Has dose form transformation (attribute) |</td><td>0</td><td>0..*</td><td>0..0</td><td>&#x3C; 736477006 | Dose form transformation (transformation) |</td></tr></tbody></table>

## Domain Information for Basic Dose Form

<table><thead><tr><th width="304.90625">Property</th><th>Value</th></tr></thead><tbody><tr><td>Domain Constraint</td><td>&#x3C;&#x3C; 736478001 | Basic dose form (basic dose form) |</td></tr><tr><td>Parent Domain</td><td>-</td></tr><tr><td>Proximal Primitive Constraint</td><td>&#x3C;&#x3C; 736478001 | Basic dose form (basic dose form) |</td></tr><tr><td>Proximal Primitive Refinement</td><td>-</td></tr></tbody></table>

#### Author View of Attributes and Ranges for Basic Dose Form

<table><thead><tr><th width="201.8333740234375">Attribute</th><th width="91.296875">Grouped</th><th width="104.5364990234375">Cardinality</th><th width="118.7552490234375">In Group Cardinality</th><th>Range Constraint</th></tr></thead><tbody><tr><td>736518005 | Has state of matter (attribute) |</td><td>0</td><td>1..1</td><td>0..0</td><td>&#x3C; 736471007 | State of matter (state of matter) |</td></tr></tbody></table>

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=SCT+Editorial+Guide&#x26;entry.670899847=Pharmaceutical%20and%20Biologic%20Product%20and%20Dose%20Form%20Attributes%20Summary" class="button primary">Provide Feedback</a>
