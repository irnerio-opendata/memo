# Motivating Scenario (Iteration 6)

## Name
Codex metadata

## Description
A codex is characterised by a series of features. First of all, a codex is identified by one or more identifiers including alphanumeric characters. Furthermore, a codex is made of one or more materials, such as parchment, paper, or a combination of both. Sometimes a particular material is also associated with specific folios or ranges of them. Moreover, a codex is characterised by having an extension in space which is expressed in terms of length and width and measured in millimeters. A second dimensional value can further refer to the set of folios that are part of the codex, or even specific ranges within that set. Finally, a codex is also characterised by a value that represents the number(s) of columns according to which the text of the manuscript(s) has been organised. Within a single codex, the number may be subject to change and may also refer to specific ranges of folios as well.

## Example 1
`codex_1` has identifier "001". It dates back to the XIII century. `binding_1`, `folio_1`, `folio_2`, `folio_3`, `folio_4` are part of it. `recto_1` and `verso_1` are part of `folio_1`. `recto_2` and `verso_2` are part of `folio_2`. `recto_3` and `verso_3` are part of `folio_3`. `recto_4` and `verso_4` are part of `folio_4`. 

`codex_2` has identifier "002". It dates back to a period between the XIV and the XV century. `binding_2`, `folio_5` and `folio_6` are part of it. `recto_5` and `verso_5` are part of `folio_5`. `recto_6` and `verso_6` are part of `folio_6`. 

`text_1` is part of `manuscript_1` (with title "Arbor cum Glossis Ioannis Phasellus") and is embodied in `folio_1` and `folio_2`. `text_2` is part of `manuscript_2` (with title "Epistula ad Barbalum") and is embodied in `folio_3` and `folio_4`. `text_3` is part of `manuscript_3` (with title "Fragmenta Decreti") and is embodied in `folio_5` and `folio_6`.

In particular:

* `binding_1` is made up by `parchment`. The height of `codex_1` is 210mm and its width is 180mm.

* `folio_1` is made up by `paper`. Its height is 210mm and its width is 180mm. It has 2 columns.

* `folio_2` is made up by `paper`. Its height is 210mm and its width is 180mm. It has 1 column.

* `folio_3` is made up by `parchment`. Its height is 210mm and its width is 180mm. It has 1 column.

* `folio_4` is made up by `parchment`. Its height is 210mm and its width is 180mm. It has 2 columns.

* `binding_2` is made up by `parchment`. The height of `codex_2` is 180mm and its width is 140mm.

* `folio_5` is made up by `parchment`. Its height is 160mm and its width is 120mm. It has 2 columns.

* `folio_6` is made up by `parchment`. Its height is 160mm and its width is 120mm. It has 2 columns.

`book_1` (with title "Vermischte Schriften"), created by `author_I`, cites `codex_1` and `codex_2`.

Given the aforementioned information:

* all the codices which are made up by folios with different materials are:
    * `codex_1`

* all the codices in which the extent of their binding is different with respect to the folios they contain are:
    * `codex_2`

* all the codices whose folios contain a variable number of columns are:
    * `codex_1`

* all the codices dating back to a period of time between the XIII and the XIV centuries are:
    * `codex_1`
    * `codex_2`

* all the titles of the manuscripts contained in codices being cited by works created by `author_I` are:
    * "Arbor cum Glossis Ioannis Phasellus"
    * "Epistula ad Barbalum"
    * "Fragmenta Decreti"