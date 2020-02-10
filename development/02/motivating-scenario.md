# Motivating Scenario (Iteration 2)

## Name
Textual metadata in time

## Description
Textual metadata in time are entities related to a manuscript that record textual information about it. They hold textual roles that fulfill certain functions in the world of discourse represented by the manuscript. In particular, textual metadata in time can assume the following textual roles:

* incipit: the context of the textual metadata in time is equivalent to a string notifying the opening words of either the manuscript text, a gloss, or both;
* explicit: the context of the textual metadata in time is equivalent to a string notifying the closing words of either the manuscript text, a gloss, or both;
* final rubric: the context of the textual metadata in time is equivalent to a textual string notifying the explicit end of either the manuscript text, a gloss, or both;

Each textual metadata is held in a certain period of time by some entity (e.g. a manuscript) and has a role assigned to it in relation to a certain textual context that is based on certain criteria. In the case of manuscripts, it is based on either the manuscript text, a gloss, or both.



## Example 1
`incipit_1`, `explicit_1` and `f_rubric_1` are related to `manuscript_1`. `incipit_2` and `explicit_2` are related to `manuscript_2`. `incipit_3` is related to `manuscript_3`.

Given that:

* `incipit_1` has content `content_incipit_1` based on `text_1` and `gloss_a`, at time 1779;

* `explicit_1` has content `content_explicit_1` based on `text_1` and `gloss_f`, at time 1780;

* `f_rubric_1` has content `content_f_rubric_1` based on `text_1`, at time 1780;

* `incipit_2` has content `content_incipit_2` based on `text_2`, at time 1861;

* `explicit_2` has content `content_explicit_2` based on `text_2`, at time 1861;

* `incipit_3` has content `content_incipit_3` based on `text_3`, at time 1800;

then:

* all the Textual Metadata In Time with role "incipit" which have been provided between 1750 and 1850 are:
    * `incipit_1`, in `manuscript_1`
    * `incipit_3`, in `manuscript_3`

* all the Textual Metadata In Time whose contents are based on only a text are:
    * `f_rubric_1`, with textual role `final rubric`, in `manuscript_1`
    * `incipit_2`, with textual role `incipit`, in `manuscript_2`
    * `explicit_2`, with textual role `explicit`, in `manuscript_2`
    * `incipit_3`, with textual role `incipit`, in `manuscript_3`
