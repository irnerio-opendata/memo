# Formal Competency Questions (Iteration 6)

## CQ_6.1
Return all the codices which are made up by folios made of different materials.

```
PREFIX : <https://w3id.org/irnerio/data/memo/>
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
Return all the codices whose binding extent is different with respect to the folios they are made up by.

```
PREFIX : <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>

SELECT DISTINCT ?codex
WHERE {
    ?codex a memo:Codex ;
           memo:hasPart ?folio , ?binding .
    ?binding a memo:Binding ;
             memo:hasExtent ?extent .
    ?extent a memo:Extent ;
            memo:hasWidth ?width ;
            memo:hasHeight ?height .
    ?folio a memo:Folio ;
           memo:hasExtent ?extent2 .
    ?extent2 a memo:Extent ;
             memo:hasWidth ?width2 ;
             memo:hasHeight ?height2 .
  FILTER ( ?width != ?width2 && ?height != ?height2 )
}
```

## CQ_6.3
Return all the codices whose folios have a variable number of columns.

```
PREFIX : <https://w3id.org/irnerio/data/memo/>
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
Return all the titles of the manuscripts contained in codices being cited by works created by `author_I`.

```
PREFIX : <https://w3id.org/irnerio/data/memo/>
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
        memo:hasCreator :author_I ;
        memo:hasTitle ?titlebook.
}
```