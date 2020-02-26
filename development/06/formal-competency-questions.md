# Formal Competency Questions (Iteration 6)

## CQ_6.1
Return all the codices in which at least one folio is made of a different material with respect to the other folios that are part of that codex.

```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>

SELECT DISTINCT ?codex
WHERE {
    ?codex a memo:Codex ;
           memo:hasPart ?folio ;
           memo:hasPart ?folio2 .
    ?folio a memo:Folio ;
           memo:hasMaterial ?a .
    ?folio2 a memo:Folio ;
           memo:hasMaterial ?b .
  FILTER (?a != ?b )
}
```

## CQ_6.2
Return all the codices in which the size measurements in terms of length and width (measured in millimeters) of their bindings are different with respect to the size measurements of the folios that are part of them.

```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>

SELECT DISTINCT ?codex
WHERE {
    ?codex a memo:Codex ;
           memo:hasPart ?folio , ?binding .
    ?binding a memo:Binding ;
             memo:hasExtent ?extent .
    ?extent a memo:Extent ;
            memo:hasWidth ?width ;
            memo:hasLength ?length .
    ?folio a memo:Folio ;
           memo:hasExtent ?extent2 .
    ?extent2 a memo:Extent ;
             memo:hasWidth ?width2 ;
             memo:hasLength ?length2 .
  FILTER ( ?width != ?width2 && ?length != ?length2 )
}
```

## CQ_6.3
Return all the codices in which at least one side of a folio has a number of columns that is different with respect the sides of the other folios that are part of that codex.

```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>

SELECT DISTINCT ?codex
WHERE {
  ?codex a memo:Codex ;
         memo:hasPart ?folio ;
         memo:hasPart ?folio2 .
  ?folio a memo:Folio ;
         memo:hasNumberOfColumns ?n .
  ?folio2 a memo:Folio ;
          memo:hasNumberOfColumns ?m .
  FILTER ( ?n != ?m )
}
```

## CQ_6.4
Return all the titles of the manuscripts contained in codices being cited by works created by `ex:author_I`, the identifier of each codex and the title of each work. 

```
PREFIX ex: <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>

SELECT DISTINCT ?title ?id ?titlebook
WHERE {
  ?manuscript a memo:Manuscript ;
              memo:hasTitle ?title ;
              memo:hasPart ?text .
  ?text a memo:Text ;
        memo:hasEmbodiment ?folio .
  ?folio a memo:Folio ;
         ^memo:hasPart ?codex .
  ?codex a memo:Codex ;
         memo:hasIdentifier ?id ;
         ^memo:cites ?book .
  ?book a memo:Book ;
        memo:hasCreator ex:author_I ;
        memo:hasTitle ?titlebook.
}
```