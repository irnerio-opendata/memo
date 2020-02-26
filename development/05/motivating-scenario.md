# Motivating Scenario (Iteration 5)

## Name
Foliation

## Description
Foliation is the numbering of the folios that are part of a codex. A folio has two parts, each called side. A side can be either a recto or a verso. Each side of a folio is identified by a string consisting of the number of the folio followed by either a “r” (for recto) or “v” (for verso).

The foliation of a codex might not be physically consequential. There could exist multiple manuscript texts in the same folio. A manuscript could exist outside the physical sequence of foliation by starting at a certain point, being interrupted by another manuscript, and then resuming after the latter ends. A manuscript could also start in a codex and continue and finish in another.

## Example 1
`folio_1`, `folio_2`, `folio_3` and `folio_4` are part of `codex_1`. `recto_1` and `verso_1` are part of `folio_1`. `recto_2` and `verso_2` are part of `folio_2`. `recto_3` and `verso_3` are part of `folio_3`. `recto_4` and `verso_4` are part of `folio_4`. In addition, `text_1` and `gloss_a`, `gloss_b`, `gloss_c`, `gloss_d`, `gloss_e`, `gloss_f` are part of `manuscript_1`. `text_2` and `gloss_g`, `gloss_h`, `gloss_i`, `gloss_l` are part of `manuscript_2`. In particular:

* `text_1` and `gloss_a`, `gloss_b`, `gloss_c` are embodied in `folio_1`;
* `text_1` and `gloss_d`, `gloss_e`, `gloss_f` are embodied in `folio_2`;
* `text_2` and `gloss_g`, `gloss_h` are embodied in `folio_3`;
* `text_2` and `gloss_i`, `gloss_l` are embodied in `folio_4`.

so:

* `gloss_b` is embodied in a given folio (`folio_1`) but refers to a text (`text_1`) that is embodied in another folio (`folio_2`);
* `gloss_g` is embodied in a given folio (`folio_3`) but refers to a text (`text_1`) that is embodied in another folio (`folio_2`).

`folio_5` and `folio_6` are part of `codex_2`. `recto_5` and `verso_5` are part of `folio_5`. `recto_6` and `verso_6` are part of `folio_6`. In addition, `text_3` and `gloss_m`, `gloss_n` are part of `manuscript_3`. In particular:

* `text_3` and `gloss_m` are embodied in `folio_5`;
* `text_3` and `gloss_n` are embodied in `folio_6`.

Given that the glosses' apparatus seen in previous iterations is still the same:

* the folios which embody second-level glosses made by `glossator_2` and that refer to or cite or annotate the `text_1` are:

    * `folio_2`, `gloss_d`;
    * `folio_2`, `gloss_e`.

## Example 2
`folio_7` is part of `codex_3`. `recto_7` and `verso_7` are part of `folio_7`. In addition, `text_4` is part of `manuscript_4`. `text_5` is part of `manuscript_5`. In particular:

* `text_4` is embodied in `folio_7`;
* `text_5` is embodied in `folio_7`.

so:

* the folios in which more than one manuscript text is embodied are:

    * `folio_7`, which is embodiment of `text_4`;
    * `folio_7`, which is embodiment of `text_5`.
