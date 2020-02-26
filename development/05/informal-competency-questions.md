# Informal Competency Questions (Iteration 5)

## Question 1

### Identifier
CQ_5.1

### Question
Return all the glosses that refer to the text embodied in `folio_2` but that are not themselves embodied in it.

### Expected outcome
A list of glosses.

### Result
* `gloss_b`
* `gloss_g`

### Based on
Example 1

## Question 2

### Identifier
CQ_5.2

### Question
Return all the folios embodying second-level glosses, which have been made by `glossator_2` and refer to or cite or annotate `text_1`, and also return the aforementioned glosses.

### Expected outcome
A list of [Folio, Gloss] pairs.

### Result
* `folio_2`, `gloss_d`
* `folio_2`, `gloss_e`

### Based on
Example 1

## Question 3

### Identifier
CQ_5.3

### Question
Return all the folios in which more than one manuscript is embodied.

### Expected outcome
A list of folios.

### Result
* `folio_7`

### Based on
Example 2