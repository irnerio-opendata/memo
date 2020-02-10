# Informal Competency Questions (Iteration 1)

## Question 1

### Identifier
CQ_1.1

### Question
Return all the glosses that are part of `manuscript_1`.

### Expected Outcome
A list of glosses.

### Result
* `gloss_a`
* `gloss_b`
* `gloss_c`
* `gloss_d`
* `gloss_e`
* `gloss_f`

### Based on
Example 1

***

## Question 2

### Identifier 
CQ_1.2

### Question
Return all the first-level glosses that are part of `manuscript_1` and cite `text_1`.

### Expected outcome
A list of glosses.

### Result
* `gloss_a`
* `gloss_f`

### Based on 
Example 1

***

## Question 3

### Identifier 
CQ_1.3

### Question
Return all the second-level glosses that are part of `manuscript_1` and that annotate or cite `text_1`.

### Expected outcome
A list of glosses.

### Result
* `gloss_c`

### Based on
Example 1

***

## Question 4

### Identifier
CQ_1.4

### Question
Return all the second-level glosses that are part of `manuscript_1` and that annotate or refer to `gloss_a`.

### Expected Outcome
A list of glosses.

### Result
* `gloss_e`
* `gloss_f`

### Based on
Example 1

***

## Question 5

### Identifier
CQ_1.5

### Question
Return all the second-level glosses that annotate or cite `text_1`.

### Expected outcome
A list of glosses.

### Result
* `gloss_c`
* `gloss_h`

### Based on
Example 2

***

## Question 6

### Identifier
CQ_1.6

### Question
Return all the third-level glosses that annotate `gloss_b`.

### Expected outcome
A list of glosses.

### Result
* `gloss_h`

### Based on
Example 2

***

## Question 7

### Identifier
CQ_1.7

### Question
Return all the glosses that cite a manuscript.

### Expected outcome
A list of glosses.

### Result
* `gloss_g`

### Based on
Example 2
