# The Medieval Manuscripts Ontology: MeMO

The Medieval Manuscripts Ontology (MeMO, https://w3id.org/irnerio/ontology/memo) is an OWL 2 DL ontology that aims to provide a framework for the formal description of the collection of medieval codices and manuscripts, managed by Progetto IRNERIO, according to certain requirements and with the possibility to extend it for representing similar resources that exist in other collections. 

MeMO has been developed by using the _Simplified Agile Methodology for Ontology Development_ (Peroni, S. (2016). SAMOD: an agile methodology for the development of ontologies. figshare. http://dx.doi.org/10.6084/m9.figshare.3189769).

This repository contains the full documentation produced during the development of MeMO. In particular:

* the `data` directory contains a set of refactored ABoxes, one for each iteration, written in the Turtle RDF serialization;

* the `development` directory contains a folder for each iteration, thus constituting a full test case with a Motivating Scenario, a list of Informal Competency Questions, a Glossary of Terms, a Graffoo diagram of the model in .png format (along with its .graphml file), a list of Formal Competency Questions, a TBox and a ABox (both written in the Turtle RDF serialization);

* the `diagrams` directory contains a set of Graffoo diagrams representing the refactored model of each iteration;

* the `docs` directory contains all the files related to the ontology and its versions in time;

* the `sparql` directory contains a set of refactored Formal Competency Questions.

![](https://github.com/irnerio-opendata/memo/blob/master/docs/current/memo.png)
