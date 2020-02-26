# Motivating Scenario (Iteration 3)

## Name
Citations

## Description
The objects that are both internal and external of the catalogue (codices, manuscripts, texts, glosses, textual metadata, catalog documents, critical editions, books, etc.) are part of a complex structure of citations and cross-references that constitute by themselves an invaluable resource for scholarly study and research support. As already seen in the Glosses iteration, a gloss can cite a number of other entities, including manuscripts, manuscript texts and other glosses. It is also very common for a manuscript to be cited by one or more critical editions. Critical editions, manuscripts and other entities are also cited in textual metadata such as the incipit, explicit and final rubric of a manuscript. 

Finally, the catalogue metadata Bibliography contains a series of citations that relate the codex the metadata is about to one or more books that have been used as references to describe that codex.

## Example 1
`manuscript_2` has `incipit_2` and `explicit_2`. `gloss_g`, `gloss_h`, `gloss_i`, `gloss_l` and `text_2` are part of `manuscript_2`. `manuscript_3` has `incipit_3`. `gloss_m`, `gloss_n` and `text_3` are part of `manuscript_3`.

Provided that:

* the gloss apparatus seen in Iteration 1 is the same, with the addition of `gloss_i` and `gloss_l`;
* the textual metadata seen in Iteration 2 are the same, with the addition of `gloss_m` and `gloss_n`;

and given that:

* `incipit_2` cites `manuscript_1`;
* `explicit_2` cites `gloss_g`;
* `gloss_g` annotates `text_2`;
* `gloss_h` annotates `text_2`;
* `gloss_i` annotates `gloss_g` and cites `edition_realization_1`, which is the realization of `edition_1`. The title of `edition_1` is "Edition One";
* `gloss_l` cites `gloss_h`, annotates `gloss_i` and cites `edition_realization_2`, which is the realization of `edition_2`. The title of `edition_2` is "Edition Two";
* `incipit_3` cites `manuscript_2`;
* `gloss_m` annotates `text_3` and cites `gloss_l`;
* `gloss_n` annotates `gloss_m` and cites `edition_realization_1`;
* `edition_realization_3` cites `manuscript_1`, `manuscript_2` and `manuscript_3`. It is the realization of `edition_3`. The title of `edition_3` is "Edition Three";

then:

* the entities cited by the textual metadata related to `manuscript_2` are:
    * `manuscript_1`
    * `gloss_g`

* the titles of the critical editions cited by second-level glosses that cite and annotate `text_2` are:
    * "Edition One"
    * "Edition Two"

* the manuscripts in which at least a second-level gloss cites the same document are:
    * `manuscript_2`
    * `manuscript_3`
