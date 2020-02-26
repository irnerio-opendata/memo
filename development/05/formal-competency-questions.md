# Informal Competency Questions (Iteration 5)

## CQ_5.1
Return all the glosses that refer to the text embodied in `ex:folio_2` but that are not embodied in it.
```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>

SELECT ?gloss
WHERE {
  ?gloss a memo:Gloss ;
         memo:hasEmbodiment ?folio ;
         memo:refersTo ?text .
  ?text a memo:Text ;
        memo:hasEmbodiment ex:folio_2 .
  ?folio a memo:Folio .
  
  FILTER ( ex:folio_2 != ?folio )
}
```

## CQ_5.2
Return all the folios embodying second-level glosses, which have been made by `ex:glossator_2` and refer to or cite or annotate `ex:text_1`, and also return the aforementioned glosses.

```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>

SELECT ?folio ?gloss
WHERE {
  ?gloss a memo:Gloss ;
         memo:hasEmbodiment ?folio ;
         memo:hasCreator ex:glossator_2 ;
         (memo:refersTo|memo:cites|memo:annotates) / (memo:refersTo|memo:cites|memo:annotates) ex:text_1 .
}
```

## CQ_5.3
Return all the folios in which more than one manuscript text is embodied.

```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>

SELECT ?folio (COUNT(?folio) AS ?count)
WHERE {
  ?manuscript memo:hasPart ?text .
  ?text a memo:Text ;
        memo:hasEmbodiment ?folio .
}
GROUP BY ?folio HAVING ( ?count > "1"^^xsd:integer )
```
