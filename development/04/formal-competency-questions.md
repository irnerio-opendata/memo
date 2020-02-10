# Formal Competency Questions (Iteration 4)

## CQ_4.1
Return all the authors of second-level glosses which annotate or cite `manuscript_1`.

```
PREFIX : <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>

SELECT ?glossator ?name

WHERE {
  
  ?gloss a memo:Gloss ;
           (memo:annotates|memo:cites) / (memo:annotates|memo:cites) :manuscript_1 ;
           memo:hasCreator ?glossator .
  ?glossator memo:hasLiteral ?literalname .
  ?literalname memo:hasLiteralValue ?name .
  
  FILTER EXISTS
         
         {
           ?gloss memo:hasCreationDate ?date .
           ?literalname memo:isValidInInterval ?interval .
           ?interval memo:hasIntervalStartDate ?start ;
                     memo:hasIntervalEndDate ?end .
    
            FILTER 

                   (
                     ?date >= ?start && 
                     ?date <= ?end 
                   )

  		  }
         
}
```

## CQ_4.2
Return all the name variants of `author_2` under which he created a manuscript, all the manuscripts he created and all the respective glossators of each manuscript.

```
PREFIX : <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>

SELECT DISTINCT ?name ?manuscript ?glossator

WHERE

{
    ?gloss a memo:Gloss ;
             ^memo:hasPart ?manuscript ;
             memo:hasCreator ?glossator .
    :author_2 ^memo:hasCreator ?manuscript ;
               memo:hasLiteral ?literal .
    ?literal memo:hasLiteralValue ?name .
    ?manuscript memo:hasCreationDate ?date .

    FILTER EXISTS

           {
             ?literal memo:isValidInInterval ?interval .
             ?interval memo:hasIntervalStartDate ?start ;
                       memo:hasIntervalEndDate ?end .

             FILTER 

             (
               ?date >= ?start && 
               ?date <= ?end
             )

           }
           
}
```