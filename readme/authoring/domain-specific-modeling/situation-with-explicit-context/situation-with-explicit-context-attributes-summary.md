# Situation with Explicit Context Attributes Summary

When authoring in this domain, these are the approved attributes and allowable ranges.

## Domain Information for Situation with Explicit Context

| Property                      | Value                                                            |
| ----------------------------- | ---------------------------------------------------------------- |
| Domain Constraint             | << `243796009 \| Situation with explicit context (situation) \|` |
| Parent Domain                 | -                                                                |
| Proximal Primitive Constraint | << `243796009 \| Situation with explicit context (situation) \|` |
| Proximal Primitive Refinement | -                                                                |

## Author View of Attributes and Ranges for Situation with Explicit Context

<table><thead><tr><th width="378.96966552734375">Attribute</th><th width="106.58673095703125">Grouped</th><th width="122.084228515625">Cardinality</th><th width="176.5633544921875">In Group Cardinality</th><th>Range Constraint</th></tr></thead><tbody><tr><td><code>408732007 | Subject relationship context (attribute) |</code></td><td>1</td><td>0..*</td><td>0..1</td><td>&#x3C;&#x3C;<code>125676002 | Person (person) |</code></td></tr><tr><td><code>408731000 | Temporal context (attribute) |</code></td><td>1</td><td>0..*</td><td>0..1</td><td>&#x3C;&#x3C; <code>410510008 | Temporal context value (qualifier value)</code> |</td></tr></tbody></table>

## Author View of Attributes and Ranges for Finding with Explicit Context

| Attribute                                      | Grouped | Cardinality | In Group Cardinality | Range Constraint                                                                  |
| ---------------------------------------------- | ------- | ----------- | -------------------- | --------------------------------------------------------------------------------- |
| 246090004 \| Associated finding (attribute) \| | 1       | 0..\*       | 0..1                 | << 272379006 \| Event (event) \| OR << 404684003 \| Clinical finding (finding) \| |
| 408729009 \| Finding context (attribute) \|    | 1       | 0..\*       | 0..1                 | << 410514004 \| Finding context value (qualifier value) \|                        |

## Author View of Attributes and Ranges for Procedure with Explicit Context

| Attribute                                        | Grouped | Cardinality | In Group Cardinality | Range Constraint                                                |
| ------------------------------------------------ | ------- | ----------- | -------------------- | --------------------------------------------------------------- |
| 363589002 \| Associated procedure (attribute) \| | 1       | 0..\*       | 0..1                 | << 71388002 \| Procedure (procedure) \|                         |
| 408730004 \| Procedure context (attribute) \|    | 1       | 0..\*       | 0..1                 | << 288532009 \| Context values for actions (qualifier value) \| |
