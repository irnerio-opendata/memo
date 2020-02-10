# Motivating Scenario (Iteration 1)

## Name
Gloss apparatus

## Description
A comment is a note added by way of comment or explanation. As regards the case study, comments are characterized by being either inside or outside a manuscript. A comment inside a manuscript is called a gloss. Glosses are marginal or interlinear handwritten comments accompanying the text of a manuscript and are an integral part of the manuscript together with its text. They were originally made to clarify or interpret the meaning of a word or passage in the text, but with time they gradually expanded in scope and assumed the role of commentaries, rich with cross-references and citations to the text, to other glosses and to other works as well.

A gloss can refer to another entity (a gloss, the text of the manuscript, an entire manuscript, etc.) in many ways, including through critical observations or citations. A gloss can also refer to more than one of these entities at the same time. The relationship which is established between these entities is characterized by a level of annotation that shifts according to the point of view taken by the scholar.

## Example 1
The following glosses are part of `manuscript_1`:

* `gloss_a`
* `gloss_b`
* `gloss_c`
* `gloss_d`
* `gloss_e`
* `gloss_f`

The text `text_1` is also part of `manuscript_1`. 

Given that:

* `gloss_a` cites `text_1` ;
* `gloss_b` refers to `text_1` ;
* `gloss_c` annotates `gloss_a` ;
* `gloss_d` refers to `gloss_a` ; 
* `gloss_e` annotates `gloss_b` and `gloss_c` ;
* `gloss_f` cites `text_1`, refers to `gloss_d` and annotates `gloss_e` ;

then:

* all the first-level glosses that are part of `manuscript_1` and cite `text_1` are:

  * `gloss_a`
  * `gloss_f`

* all the second-level glosses that are part of `manuscript_1` and that annotate or cite `text_1` are:

  * `gloss_c`

* all the second-level glosses that are part of `manuscript_1` and that annotate or refer to `gloss_a` are:

  * `gloss_e`
  * `gloss_f`

## Example 2
A `gloss_g` and a `gloss_h` are part of `manuscript_2`. 

Given that:

* `gloss_g` cites `manuscript_1` and refers to `text_1`;
* `gloss_h` refers to `gloss_e` and annotates `gloss_f`;

then:

* all the second-level glosses that annotate or cite `text_1` are:

    * `gloss_c`
    * `gloss_h`

* all the third-level glosses that annotate `gloss_b` are:

    * `gloss_h`

* all the glosses that cite a manuscript are:

    * `gloss_g`
