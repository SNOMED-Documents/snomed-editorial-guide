---
layout:
  width: wide
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
    visible: true
---

# Evaluation Procedure Attributes

The following defining attributes are unique in the context of the 386053000 |Evaluation procedure (procedure)| subhierarchy. Many of these attributes (e.g., Component, Scale type) are used to define Observable entity concepts. Evaluation procedures may use the attributes below in addition to those attributes allotted to the [71388002 | Procedure (procedure)|](http://snomed.info/id/71388002) hierarchy (see _Procedure Attributes Summary_ page). All of the attributes for Evaluation procedure concepts should be grouped. Some of the current modeling does not reflect this guidance. The future of this hierarchy in relation to the observable entity hierarchy is under review. See 'Observable Entity vs. Evaluation Procedure' at [Observable Entity](../../../../../../authoring/procedure/Observable-Entity_174690597.html).

## Component

Component refers to what is being observed or measured by a procedure.

For example,

* [442091000 | Measurement of ethanol using gas chromatography (procedure)|](http://snomed.info/id/442091000) has [246093002 | Component (attribute)|](http://snomed.info/id/246093002) of [419442005 | Ethanol (substance)|](http://snomed.info/id/419442005)

<figure><img src="../../../../../../authoring/procedure/images/250545868.png" alt=""><figcaption><p>Figure 1. Inferred view of 442091000 |Measurement of ethanol using gas chromatography (procedure)|</p></figcaption></figure>

Although Pharmaceutical / biologic product (product) and its descendants are considered valid values for the Component (attribute), they are not currently used as values for this attribute in the International Release. The only exception is 787859002 |Vaccine product (medicinal product)| and its descendants, which are used as valid values for this attribute.

## Has specimen

_Has Specimen_ indicates the type of specimen on which a measurement or observation is performed.

For example,

* [442165003 | Quantitative measurement of polychlorinated biphenyl in blood specimen using gas chromatography (procedure)|](http://snomed.info/id/442165003) uses [116686009 | Has specimen (attribute)|](http://snomed.info/id/116686009) of [119297000 | Blood specimen (specimen)|](http://snomed.info/id/119297000)

## Measurement method

_Measurement Method_ specifies the method by which an evaluation procedure is performed. It provides additional specificity. For measurement procedures, the [260686004 | Method (attribute)|](http://snomed.info/id/260686004) is given the value [129266000 | Measurement - action (qualifier value)|](http://snomed.info/id/129266000) . No concept can be defined with a [370129005 | Measurement method (attribute)|](http://snomed.info/id/370129005) unless it is being used to refine a \_[ 260686004 | Method (attribute)|](http://snomed.info/id/260686004) \_ that has a value of \_[ 129266000 | Measurement - action (qualifier value)|](http://snomed.info/id/129266000) \_or one of its subtypes that is also specified in the concept definition. That is, use of \_[ 370129005 | Measurement method (attribute)|](http://snomed.info/id/370129005) \_ must be**in addition** to a \_[ 260686004 | Method (attribute)|](http://snomed.info/id/260686004) \_ of \_[ 129266000 | Measurement - action (qualifier value)|](http://snomed.info/id/129266000) \_or one of its subtypes.

Also, the [370129005 | Measurement method (attribute)|](http://snomed.info/id/370129005) and its value must be grouped with the [260686004 | Method (attribute)|](http://snomed.info/id/260686004) and its value of the concept or subtype of [129266000 | Measurement - action (qualifier value)|](http://snomed.info/id/129266000) .

For example,

* [442165003 | Quantitative measurement of polychlorinated biphenyl in blood specimen using gas chromatography (procedure)|](http://snomed.info/id/442165003) has a [370129005 | Measurement method (attribute)|](http://snomed.info/id/370129005) of [2842000 | Gas chromatography measurement (procedure)|](http://snomed.info/id/2842000)

<figure><img src="../../../../../../authoring/procedure/images/250545866.png" alt=""><figcaption><p>Figure 2. Stated view of 442165003 |Quantitative measurement of polychlorinated biphenyl in blood specimen using gas chromatography (procedure)|</p></figcaption></figure>

## Property

_Property_ specifies the kind of property (quality or characteristic) being measured.

For example,

* [19165008 | Measurement of limb length (procedure)|](http://snomed.info/id/19165008) has a [370130000 | Property (attribute)|](http://snomed.info/id/370130000) of [410668003 | Length property (qualifier value)|](http://snomed.info/id/410668003)

<figure><img src="../../../../../../authoring/procedure/images/250545865.png" alt=""><figcaption><p>Figure 3. Stated view of 19165008 |Measurement of limb length (procedure)|</p></figcaption></figure>

## Scale type

_Scale Type_ refers to the scale of the result of an observation of a diagnostic test.

For example,

* [442165003 | Quantitative measurement of polychlorinated biphenyl in blood specimen using gas chromatography (procedure)|](http://snomed.info/id/442165003) has [370132008 | Scale type (attribute)|](http://snomed.info/id/370132008) of [30766002 | Quantitative (qualifier value)|](http://snomed.info/id/30766002)

## Time aspect

_Time Aspect_ specifies temporal relationships \_\_ for a measurement procedure. While this attribute has been approved, guidelines for its implementation await development.

## Further clarification

An evaluation procedure may evaluate a property of a component, or a property may be the sole focus of the method. In the latter case, component isn’t included since only the property is being evaluated.

For example - an evaluation procedure evaluating a property of a component:

* [443834000 | Quantitative measurement of mass concentration of bismuth in urine specimen (procedure)|](http://snomed.info/id/443834000) has [370130000 | Property (attribute)|](http://snomed.info/id/370130000) of [118539007 | Mass concentration (property) (qualifier value)|](http://snomed.info/id/118539007) and [246093002 | Component (attribute)|](http://snomed.info/id/246093002) of [23172004 | Bismuth (substance)|](http://snomed.info/id/23172004)

<figure><img src="../../../../../../authoring/procedure/images/250545867.png" alt=""><figcaption><p>Figure 4. Inferred view of 443834000 |Quantitative measurement of mass concentration of bismuth in urine specimen (procedure)|</p></figcaption></figure>

For example - where property may be the sole focus of the method:

* [78888000 | Osmolality measurement, urine (procedure)|](http://snomed.info/id/78888000)

<figure><img src="../../../../../../authoring/procedure/images/174691353.png" alt=""><figcaption><p>Figure 5. Inferred view of 78888000 |Osmolality measurement, urine (procedure)|</p></figcaption></figure>
