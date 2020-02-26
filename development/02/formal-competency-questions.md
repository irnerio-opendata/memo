# Formal Competency Questions (Iteration 2)

## CQ_2.1
Return all the textual metadata in time with textual role "incipit" which have been provided between 1750 and 1850 and the manuscripts they are related to.
```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>

SELECT ?tmit ?manuscript
WHERE {
  ?tmit a memo:TextualMetadataInTime ;
		    ^memo:hasTextualMetadata ?manuscript ;
        memo:withTextualRole memo:incipit ;
        memo:atTime ?time .
  ?time memo:hasIntervalStartDate ?date .
  FILTER
  (
    ?date > "1750"^^xsd:gYear && 
    ?date < "1850"^^xsd:gYear
  )
}
```

## CQ_2.2
Return all the textual metadata in time whose context is based only on a text, their respective textual roles and the manuscripts they are related to.

```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>

SELECT ?tmit ?role ?manuscript
WHERE {
  ?tmit a memo:TextualMetadataInTime ;
		    ^memo:hasTextualMetadata ?manuscript ;
        memo:withTextualRole ?role ;
        memo:relatesToTextualContext ?context .
  FILTER NOT EXISTS
  {
    ?text a memo:Gloss .
    ?context memo:isBasedOn ?text .
  }
}
```

## CQ_2.3
Return all the textual metadata in time which have been created by `ex:agent_1` starting from 1780, their textual roles, their dates and the manuscripts they are related to.

```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>

SELECT ?tmit ?role ?date ?manuscript
WHERE {
  ?tmit a memo:TextualMetadataInTime ;
		    ^memo:hasTextualMetadata ?manuscript ;
        memo:withTextualRole ?role ;
        memo:hasCreator ex:agent_1 ;
        memo:atTime ?time .
  ?time memo:hasIntervalStartDate ?date .
  FILTER ( ?date >= "1780"^^xsd:gYear )
}
```