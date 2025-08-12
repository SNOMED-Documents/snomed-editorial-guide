# Clinical drug

The Clinical Drug "containing precisely" (CD-precise) concept is an abstract representation of the precise active ingredient, basis of strength substance (BoSS), strength, and manufactured dose form of a drug product. It implies that the drug product must contain only the precise active ingredient(s) specified in the FSN. 

  * [Clinical Drug with Discrete Dose Form](Clinical-Drug-with-Discrete-Dose-Form_225055220.html)
  * [Clinical Drug with Continuous Dose Form](Clinical-Drug-with-Continuous-Dose-Form_225055251.html)

The guidance below applies to both discrete and continuous dose forms. 

## Descriptions

Align FSN and PT naming and case sensitivity with the concepts selected as attribute values. 

For multiple-ingredient drug products, the BoSS must be in alphabetical order and separated by the word “and”.

The following units of measure should not be abbreviated in any descriptions; always spell out:

  * microequivalent
  * microliter
  * microgram
  * microliter (with GB spelling microlitre)
  * million unit
  * nanogram
  * picogram
  * unit

Synonyms matching the FSN are not required. 

## Concentration strength units

For solids and semi-solids, a concentration strength will be mass/mass (weight/weight) – usually mg/g.

  * Solid = pill, tablet, suppository, tape, patch, lozenge, implant, gum, capsule, etc.
  * Semi-solid = cement, cream, gel, ointment, paste, poultice

For liquids, a concentration strength will be mass/volume (weight/volume) – usually mg/mL.

  * Liquid = solution, suspension, tincture, spirit, emulsion, foam, lotion, oil, lacquer, etc.

Requests for new concepts that conflict with the above require a clear justification for the variance.

## International Unit

 _International Unit_ as a description is arbitrary, and to be understood, each product requires reference to a particular bioefficacy specification for that entity. Therefore,  _international_ _unit_ is neither a meaningful nor comparable description at Clinical Drug level. International unit will be represented as  _unit_ in Clinical Drug descriptions. Abbreviations will not be used.

For example,

  *     * 1237145006 |Product containing precisely octocog alfa 1000 unit/1 vial powder for conventional release solution for injection (clinical drug)|
    * PT - Octocog alfa 1000 unit powder for solution for injection vial

The |Has presentation strength numerator unit| will still continue to have a value of |International unit (qualifier value)| even though  _unit_ is stated in the FSN and PT.

## Product strength _not equal to_

Concepts with product strength that is "not equal to" are modeled as primitive, with attributes added as described in the corresponding subpages, except that strength numerator attributes will not be added. The appropriate Medicinal Product Form-only (MPF-only) concept will infer as a parent.

## Product strength numerator values

Expression of product strength in metric units is preferred.

To avoid semantically equivalent concepts, product strength for metric units are normalized as follows:

  *     * Use milligram if value is <1000; if  _>_ 1000, convert to gram.
    * Use microgram if value is <1000; if  _>_ 1000, convert to milligram.
    * Use nanogram if value is <1000; if  _>_ 1000, convert to microgram.  

    * Use picogram if value is <1000; if  _>_ 1000, convert to nanogram.

Similarly, if a unit is less than one, convert to a smaller unit. gram → milligram → microgram → nanogram → picogram

For example, 

If the value is less than one gram, convert value to milligrams. 

To avoid semantically equivalent concepts, product strength for units are normalized as follows:

  * Use million unit if value is  _>_ 1000000 unit

The following units are not allowed unless specifically noted as an exception:

  *     * 408165007 |Mega u (qualifier value)|

Repeating decimals are rounded to three decimal places (with 5 and above rounded up and 4 and below rounded down).

## Precise active ingredient

The _Precise Active Ingredient_ (PAI) cannot be modeled as a substance hydrate or solvate unless the BoSS is expressed as a substance hydrate or solvate.

Concepts containing pancreatic enzymes are modeled based on the discrete enzymes; because of variability between real clinical drugs, synonyms representing a total amount in a particular product will not be included in the International Release.

## Inference based on dose form

Clinical drugs _containing precisely x_ are modeled with a count based on the  _substance(s)_ to support a closed world view (i.e., a count of 1 will not infer a count of 2). The closed world view does not apply to dose forms. A very rare case can arise where, for example, a clinical drug that is for an _x ear and eye drop_ is a subtype of both the clinical drug _x eye drop_ and the clinical drug _x ear drop_. This makes real world sense where all descendants of _x clinical drug eye drop_ are for use in the eye, and a small subgroup of them may also be acceptable for use in the ear.

For example,

1220547004 |Product containing precisely gentamicin (as gentamicin sulfate) 3 milligram/1 milliliter conventional release eye drops (clinical drug)| correctly infers a subtype of 1142217003 |Product containing precisely gentamicin (as gentamicin sulfate) 3 milligram/1 milliliter conventional release ear and eye drops (clinical drug)|.

## Anhydrous

When a clinical drug has a BoSS specified in a Summary of Product Characteristics as an anhydrous substance, the PAI is represented as the unmodified substance, i.e., the substance with an unspecified level of hydration. 

For example,

  *     * 1153520006 |Product containing precisely **carbidopa anhydrous (as carbidopa)** 25 milligram and levodopa 250 milligram/1 each conventional release oral tablet (clinical drug)|

[The SPC](https://www.medicines.org.uk/emc/product/7805/smpc#gref) states each tablet "contains 27.0 mg **carbidopa (equivalent to 25 mg of anhydrous carbidopa)** and 250 mg levodopa." The BoSS is anhydrous carbidopa, so the PAI is Carbidopa. 

  

  *     * 1331919008 |Product containing precisely carbidopa anhydrous (as carbidopa) 12.5 milligram and entacapone 200 milligram and levodopa 50 milligram/1 each conventional release oral tablet (clinical drug)|

[This SPC](https://www.hpra.ie/img/uploaded/swedocuments/Licence_PA0711-252-001_09032021145258.pdf) states, "Each film-coated tablet contains 50 mg of levodopa, 12.5 mg of **carbidopa anhydrous (as 13.5 mg carbidopa monohydrate)** and 200 mg of entacapone." The Boss is anhydrous carbidopa, so the PAI is Carbidopa. 

  

  

  

  

