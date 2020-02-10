# Informal Competency Questions (Iteration 2)

## Question 1

### Identifier
Q_2.1

### Question
Return all the textual metadata in time with textual role "incipit" which have been provided between 1750 and 1850 and the manuscripts that have them.

### Expected outcome
A list of [Textual Metadata In Time , Manuscript] pairs.

### Result
* `incipit_1`, `manuscript_1`
* `incipit_3`, `manuscript_3`

### Based on
Example 1

## Question 2

### Identifier
Q_2.2

### Question
Return all the textual metadata in time whose contents are based only on a text, their respective textual roles and the manuscripts that have them.

### Expected outcome
A list of [Textual Metadata In Time, Textual Role, Manuscript] triples.

### Result
* `f_rubric_1`, `final rubric`, `manuscript_1`
* `incipit_2`, `incipit`, `manuscript_2`
* `explicit_2`, `explicit`, `manuscript_2`
* `incipit_3`, `incipit`, `manuscript_3`

### Based on
Example 1
