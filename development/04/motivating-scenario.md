# Motivating Scenario (Iteration 4)

## Name
Names

## Description
The name of a creator of one or more resources (e.g. a manuscript, gloss, textual metadata, critical edition, etc.) could change, due to the use of pseudonyms (a fairly common practice at the time), nicknames and similar types of variations over time.

## Example 1
Provided that the gloss and textual metadata in time seen in Iteration 3 are the same, and given that:

* `gloss_a`, `gloss_b` and `gloss_c` have been created by `glossator_1`, where:
    * `gloss_a` has been created in 1240 under the name _Ioannis Phasellus_;
    * `gloss_b` has been created in 1241 under the name _Ioannis Phasellus_;
    * `gloss_c` has been created in 1250 under the name _Ioannis Phasellus_.

* `gloss_d`, `gloss_e` and `gloss_f` have been created by `glossator_2`, where:
    * `gloss_d` has been created in 1261 under the name _Farnese de Vandimion_;
    * `gloss_e` has been created in 1265 under the name _Farnese_;
    * `gloss_f` has been created in 1266 under the name _Farnese_.

* `gloss_g` and `gloss_h` have been created by `glossator_3`, where:
    * `gloss_g` has been created in 1270 under the name _Boscogne_;
    * `gloss_h` has been created in 1271 under the name _Boscone_.

* `gloss_i` and `gloss_l` have been created by `glossator_4`, where:
    * `gloss_i` has been created in 1276 under the name _Griffith_;
    * `gloss_l` has been created in 1280 under the name _Femto_.

* `gloss_m` and `gloss_n` have been created by `glossator_5`, where:
    * `gloss_m` has been created in 1285 under the name _Gattsu_;
    * `gloss_n` has been created in 1289 under the name _Guts_.

* `manuscript_1` has been created in 1001 by `author_1` under the name _Barbalo_.

* `manuscript_2` and `manuscript_3` have been created by `author_2`, where:
    * `manuscript_2` has been created in 1012 under the name _Serpico_.
    * `manuscript_3` has been created in 1014 under the name _Serpico_.
    * other variants of `author_2`'s name are _Serpicus_ and _Sorbo Serpico_.

then:

* all the authors that created second-level glosses which annotate or cite `manuscript_1` are:
    * `glossator_3`, under the name _Boscogne_;

* all the name variants of `author_2` under which they created a manuscript, all the manuscripts they created and all the respective glossators of each manuscript are:
    * _Serpico_
    * `manuscript_2`, `manuscript_3`
    * `glossator_3`, `glossator_4`, `glossator_5`
