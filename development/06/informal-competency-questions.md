# Informal Competency Questions (Iteration 6)

## Question 1

### Identifier
CQ_6.1

### Question
Return all the codices in which at least one folio is made of a different material with respect to the other folios.

### Expected outcome
A list of codices.

### Result
* `codex_1`

### Based on
Example 1

## Question 2

### Identifier
CQ_6.2

### Question
Return all the codices whose binding size measurement (measured in millimeters) is different with respect to the folios they are made up by.

### Expected outcome
A list of codices.

### Result
* `codex_2`

## Question 3

### Identifier
CQ_6.3

### Question
Return all the codices in which at least one side of a folio has a number of columns that is different with respect the sides of the other folios.

### Expected outcome
A list of codices.

### Result
* `codex_1`

## Question 4

### Identifier
CQ_6.4

### Question
Return all the titles of the manuscripts contained in codices being cited by works created by `author_I`, the identifier of each codex and the title of each work. 

### Expected outcome
A list of [Manuscript title, Identifier, Book title] triples.

### Result
* "Arbor cum Glossis Ioannis Phasellus", "001", "Vermischte Schriften"
* "Epistula ad Barbalum", "001", "Vermischte Schriften"
* "Fragmenta Decreti", "002", "Vermischte Schriften"