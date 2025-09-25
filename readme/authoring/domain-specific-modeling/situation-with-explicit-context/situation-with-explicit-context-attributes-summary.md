# Situation with Explicit Context Attributes Summary

When authoring in this domain, these are the approved attributes and allowable ranges.

## Domain Information for Situation with Explicit Context

<table><thead><tr><th width="312.8411865234375">Property</th><th>Value</th></tr></thead><tbody><tr><td>Domain Constraint</td><td>&#x3C;&#x3C; 243796009 | Situation with explicit context (situation) |</td></tr><tr><td>Parent Domain</td><td>-</td></tr><tr><td>Proximal Primitive Constraint</td><td>&#x3C;&#x3C; 243796009 | Situation with explicit context (situation) |</td></tr><tr><td>Proximal Primitive Refinement</td><td>-</td></tr></tbody></table>

## Author View of Attributes and Ranges for Situation with Explicit Context

<table><thead><tr><th width="335.01556396484375">Attribute</th><th width="104.67694091796875">Grouped</th><th width="119.3323974609375">Cardinality</th><th width="175.4696044921875">In Group Cardinality</th><th width="303.2647705078125">Range Constraint</th></tr></thead><tbody><tr><td>408732007 |Subject relationship context (attribute)|</td><td>1</td><td>0..*</td><td>0..1</td><td>&#x3C;&#x3C;125676002 | Person (person) |</td></tr><tr><td>408731000 | Temporal context (attribute) |</td><td>1</td><td>0..*</td><td>0..1</td><td>&#x3C;&#x3C; 410510008 | Temporal context value (qualifier value) |</td></tr></tbody></table>

## Author View of Attributes and Ranges for Finding with Explicit Context

<table><thead><tr><th width="398.205810546875">Attribute</th><th width="106.09033203125">Grouped</th><th width="120.2135009765625">Cardinality</th><th width="181.2335205078125">In Group Cardinality</th><th width="263.5164794921875">Range Constraint</th><th></th></tr></thead><tbody><tr><td>246090004 | Associated finding (attribute) |</td><td>1</td><td>0..*</td><td>0..1</td><td>&#x3C;&#x3C; <code>272379006 | Event (event) |</code> OR &#x3C;&#x3C; <code>404684003 | Clinical finding (finding) |</code></td><td></td></tr><tr><td>408729009 | Finding context (attribute) |</td><td>1</td><td>0..*</td><td>0..1</td><td>&#x3C;&#x3C; <code>410514004 | Finding context value (qualifier value) |</code></td><td></td></tr></tbody></table>

## Author View of Attributes and Ranges for Procedure with Explicit Context

| Attribute                                        | Grouped | Cardinality | In Group Cardinality | Range Constraint                                                |
| ------------------------------------------------ | ------- | ----------- | -------------------- | --------------------------------------------------------------- |
| 363589002 \| Associated procedure (attribute) \| | 1       | 0..\*       | 0..1                 | << 71388002 \| Procedure (procedure) \|                         |
| 408730004 \| Procedure context (attribute) \|    | 1       | 0..\*       | 0..1                 | << 288532009 \| Context values for actions (qualifier value) \| |
