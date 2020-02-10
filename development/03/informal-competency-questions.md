# Informal Competency Questions (Iteration 3)

## Question 1

### Identifier
CQ_3.1

### Question
Return the entities cited by the textual metadata in time of `manuscript_2`.

### Expected outcome
A list of entities.

### Result
* `manuscript_1`
* `gloss_g`

### Based on
Example 1

***

## Question 2

### Identifier
CQ_3.2

### Question
Return all the titles of the critical editions cited by second-level glosses that cite or annotate `text_2`.

### Expected outcome
A list of titles.

### Result
* "Edition One"
* "Edition Two"

### Based on
Example 1

***

## Question 3

### Identifier
CQ_3.3

### Question
Return all the manuscripts in which at least a second-level gloss that annotates a text also cites the same critical edition.

### Expected outcome
A list of manuscripts.

### Result
* `manuscript_2`
* `manuscript_3`

### Based on
Example 1