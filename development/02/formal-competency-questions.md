# Formal Competency Questions (Iteration 2)

## CQ_2.1
Return all the textual metadata in time with textual role "incipit" which have been provided between 1750 and 1850 and the manuscripts they are related to.
```
PREFIX : <https://github.com/irnerio-opendata/memo/development/02/ABox.ttl/>
PREFIX memo: <https://github.com/irnerio-opendata/memo/development/02/TBox.ttl/>
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
Return all the textual metadata in time whose contents are based only on a text, their respective textual roles and the manuscripts they are related to.

```
PREFIX : <https://github.com/irnerio-opendata/memo/development/02/ABox.ttl/>
PREFIX memo: <https://github.com/irnerio-opendata/memo/development/02/TBox.ttl/>

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
