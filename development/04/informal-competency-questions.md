# Informal Competency Questions (Iterations 4)

## Question 4.1

### Identifier
CQ_4.1

### Question
Return all the authors of second-level glosses which annotate or cite `manuscript_1`.

### Expected outcome
A list of [Person, Name] pairs.

### Result
* `glossator_4`, "Guriffis";

### Based on
Example 1

***

## Question 4.2

### Identifier
CQ_4.2

### Question
Return all the name variants of `author_2` under which he created a manuscript, all the manuscripts he created and all the respective glossators of each manuscript.

### Expected outcome
A list of [Name, Manuscript, Person] triples.

### Result
* "Serpico", `manuscript_2`, `glossator_3`
* "Serpico", `manuscript_2`, `glossator_4`
* "Serpico", `manuscript_3`, `glossator_5` 

### Based on
Example 1