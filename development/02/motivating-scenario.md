# Motivating Scenario (Iteration 2)

## Name
Textual metadata in time

## Description
Metadata that record textual information are not fixed. Each metadata is created by some agent, is held in a certain period by some entity (e.g. a manuscript) and has a value assigned to it within a particular context. In fact, metadata change in time and layer on the top of each other, thus creating a record of various interpretations with respect to certain aspects of that resource. Thus, it is of the utmost importance to keep track of these changes. In the case of manuscripts, these metadata can assume the following values:

* incipit: the context of the textual metadata in time is equivalent to a string notifying the opening words of either the manuscript text, a gloss, or both;
* explicit: the context of the textual metadata in time is equivalent to a string notifying the closing words of either the manuscript text, a gloss, or both;
* final rubric: the context of the textual metadata in time is equivalent to a textual string notifying the explicit end of either the manuscript text, a gloss, or both.

Also, if the metadata refers to a manuscript, the context is based on either the manuscript text, a gloss, or both.

## Example 1
`manuscript_1` has `incipit_1`, `explicit_1` and `f_rubric_1`. `manuscript_2` has `incipit_2` and `explicit_2`. `manuscript_3` has `incipit_3`. Given that:

* `incipit_1` has context based on `text_1` and `gloss_a`, at time 1779. It has been created by `agent_1`;

* `explicit_1` has context based on `text_1` and `gloss_f`, at time 1780. It has been created by `agent_1`;

* `f_rubric_1` has context based on `text_1`, at time 1780. It has been created by `agent_1`;

* `incipit_2` has context based on `text_2`, at time 1861. It has been created by `agent_2`;

* `explicit_2` has context based on `text_2`, at time 1861. It has been created by `agent_2`;

* `incipit_3` has context based on `text_3`, at time 1800. It has been created by `agent_1`.

then:

* all the metadata with role "incipit" which have been provided between 1750 and 1850 are:
    * `incipit_1`, in `manuscript_1`;
    * `incipit_3`, in `manuscript_3`;

* all the metadata whose contents are based on only a text are:
    * `f_rubric_1`, with textual role `final rubric`, in `manuscript_1`;
    * `incipit_2`, with textual role `incipit`, in `manuscript_2`;
    * `explicit_2`, with textual role `explicit`, in `manuscript_2`;
    * `incipit_3`, with textual role `incipit`, in `manuscript_3`;

* all the metadata provided by `agent_1` starting from 1780, along with their textual roles, their dates and the manuscripts they are related to are:
    * `explicit_1`, `explicit`, 1780, `manuscript_1`;
    * `f_rubric_1`, `final rubric`, 1780, `manuscript_1`;
    * `incipit_3`, `incipit`, 1800, `manuscript_3`.
