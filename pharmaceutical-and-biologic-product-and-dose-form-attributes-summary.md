# Pharmaceutical and Biologic Product and Dose Form Attributes Summary

When authoring in this domain, these are the approved attributes and allowable ranges. They are the Human Readable Concept Model (HRCM).  

| Domain Information for 373873005 \| Pharmaceutical / biologic product (product) \| |   |
|---|---|
| Domain Constraint | << 373873005 \| Pharmaceutical / biologic product (product) \| |
| Parent Domain | - |
| Proximal Primitive Constraint | << 373873005 \| Pharmaceutical / biologic product (product) \| |
| Proximal Primitive Refinement | - |

  

| Author View of Attributes and Ranges for 373873005 \| Pharmaceutical / biologic product (product) \| |   |   |   |   |
|---|---|---|---|---|
| Attribute | Grouped | Cardinality | In Group Cardinality | Range Constraint |
| 1142140007 \| Count of active ingredient (attribute) \| | 0 | 0..1 | 0..0 | int(>#0..) |
| 1142141006 \| Count of base and modification pair (attribute) \| | 0 | 0..1 | 0..0 | int(>#0..) |
| 1142139005 \| Count of base of active ingredient (attribute) \| | 0 | 0..1 | 0..0 | int(>#0..) |
| 127489000 \| Has active ingredient (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| |
| 732943007 \| Has basis of strength substance (attribute) \| | 1 | 0..* | 0..1 | < 105590001 \| Substance (substance) \| |
| 733722007 \| Has concentration strength denominator unit (attribute) \| | 1 | 0..* | 0..1 | < 767524001 \| Unit of measure (qualifier value) \| |
| 1142137007 \| Has concentration strength denominator value (attribute) \| | 1 | 0..* | 0..1 | dec(>#0..) |
| 733725009 \| Has concentration strength numerator unit (attribute) \| | 1 | 0..* | 0..1 | < 767524001 \| Unit of measure (qualifier value) \| |
| 1142138002 \| Has concentration strength numerator value (attribute) \| | 1 | 0..* | 0..1 | dec(>#0..) |
| 762951001 \| Has ingredient (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| |
| 860779006 \| Has ingredient characteristic (attribute) \| | 1 | 0..* | 0..* | << 362981000 \| Qualifier value (qualifier value) \| |
| 1149366004 \| Has ingredient qualitative strength (attribute) \| | 1 | 0..* | 0..1 | < 1149484003 \| Ingredient qualitative strength (qualifier value) \| |
| 411116001 \| Has manufactured dose form (attribute) \| | 0 | 0..1 | 0..0 | << 736542009 \| Pharmaceutical dose form (dose form) \| |
| 762949000 \| Has precise active ingredient (attribute) \| | 1 | 0..* | 0..1 | << 105590001 \| Substance (substance) \| |
| 732947008 \| Has presentation strength denominator unit (attribute) \| | 1 | 0..* | 0..1 | < 767524001 \| Unit of measure (qualifier value) \| |
| 1142136003 \| Has presentation strength denominator value (attribute) \| | 1 | 0..* | 0..1 | dec(>#0..) |
| 732945000 \| Has presentation strength numerator unit (attribute) \| | 1 | 0..* | 0..1 | < 767524001 \| Unit of measure (qualifier value) \| |
| 1142135004 \| Has presentation strength numerator value (attribute) \| | 1 | 0..* | 0..1 | dec(>#0..) |
| 860781008 \| Has product characteristic (attribute) \| | 0 | 0..* | 0..0 | << 362981000 \| Qualifier value (qualifier value) \| |
| 774158006 \| Has product name (attribute) \| | 0 | 0..1 | 0..0 | << 774167006 \| Product name (product name) \| |
| 774159003 \| Has supplier (attribute) \| | 0 | 0..1 | 0..0 | << 774164004 \| Supplier (supplier) \| |
| 1149367008 \| Has target population (attribute) \| | 0 | 0..1 | 0..0 | < 27821000087106 \| Product target population (qualifier value) \| |
| 763032000 \| Has unit of presentation (attribute) \| | 0 | 0..1 | 0..0 | << 732935002 \| Unit of presentation (unit of presentation) \| |
| 766939001 \| Plays role (attribute) \| | 0 | 0..* | 0..0 | << 766940004 \| Role (role) \| |
| 1148793005 \| Unit of presentation size quantity (attribute) \| | 0 | 0..1 | 0..0 | dec(>#0..) |
| 320091000221107 \| Unit of presentation size unit (attribute) \| | 0 | 0..1 | 0..0 | << 767524001 \| Unit of measure (qualifier value) \| |

  

| Domain Information for 781405001 \| Medicinal product package (product) \| |   |
|---|---|
| Domain Constraint | << 781405001 \| Medicinal product package (product) \| |
| Parent Domain | 373873005 \| Pharmaceutical / biologic product (product) \| |
| Proximal Primitive Constraint | << 781405001 \| Medicinal product package (product) \| |
| Proximal Primitive Refinement | - |

  

| Author View of Attributes and Ranges for 781405001 \| Medicinal product package (product) \| |   |   |   |   |
|---|---|---|---|---|
| Attribute | Grouped | Cardinality | In Group Cardinality | Range Constraint |
| 774160008 \| Contains clinical drug (attribute) \| | 1 | 1..* | 1..1 | << 763158003 \| Medicinal product (product) \| |
| 1142143009 \| Count of clinical drug type (attribute) \| | 0 | 1..1 | 0..0 | int(>#0..) |
| 1142142004 \| Has pack size (attribute) \| | 1 | 0..* | 0..1 | dec(>#0..) |
| 774163005 \| Has pack size unit (attribute) \| | 1 | 0..* | 0..1 | << 767524001 \| Unit of measure (qualifier value) \| |

  

| Domain Information for 736542009 \| Pharmaceutical dose form (dose form) \| |   |
|---|---|
| Domain Constraint | << 736542009 \| Pharmaceutical dose form (dose form) \| |
| Parent Domain | - |
| Proximal Primitive Constraint | << 736542009 \| Pharmaceutical dose form (dose form) \| |
| Proximal Primitive Refinement | - |

  

| Author View of Attributes and Ranges for 736542009 \| Pharmaceutical dose form (dose form) \| |   |   |   |   |
|---|---|---|---|---|
| Attribute | Grouped | Cardinality | In Group Cardinality | Range Constraint |
| 736476002 \| Has basic dose form (attribute) \| | 0 | 0..1 | 0..0 | < 736478001 \| Basic dose form (basic dose form) \| |
| 736472000 \| Has dose form administration method (attribute) \| | 0 | 0..* | 0..0 | < 736665006 \| Dose form administration method (administration method) \| |
| 736474004 \| Has dose form intended site (attribute) \| | 0 | 0..* | 0..0 | < 736479009 \| Dose form intended site (intended site) \| |
| 736475003 \| Has dose form release characteristic (attribute) \| | 0 | 0..1 | 0..0 | < 736480007 \| Dose form release characteristic (release characteristic) \| |
| 736473005 \| Has dose form transformation (attribute) \| | 0 | 0..* | 0..0 | < 736477006 \| Dose form transformation (transformation) \| |

  

| Domain Information for 736478001 \| Basic dose form (basic dose form) \| |   |
|---|---|
| Domain Constraint | << 736478001 \| Basic dose form (basic dose form) \| |
| Parent Domain | - |
| Proximal Primitive Constraint | << 736478001 \| Basic dose form (basic dose form) \| |
| Proximal Primitive Refinement | - |

  

| Author View of Attributes and Ranges for 736478001 \| Basic dose form (basic dose form) \| |   |   |   |   |
|---|---|---|---|---|
| Attribute | Grouped | Cardinality | In Group Cardinality | Range Constraint |
| 736518005 \| Has state of matter (attribute) \| | 0 | 1..1 | 0..0 | < 736471007 \| State of matter (state of matter) \| |

  

