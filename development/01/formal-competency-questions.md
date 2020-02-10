# Formal Competency Questions

## CQ_1.1
Return all the glosses that are part of `manuscript_1`.

```
PREFIX : <https://w3id.org/irnerio/data/memo/> 
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/> 

SELECT ?gloss

WHERE {

  ?gloss a memo:Gloss .
  ?gloss ^memo:hasPart :manuscript_1
  
}
```

## CQ_1.2
Return all the first-level glosses that are part of `manuscript_1` and cite `text_1`.

```
PREFIX : <https://w3id.org/irnerio/data/memo/> 
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/> 

SELECT ?gloss

WHERE {

  ?gloss a memo:Gloss .
  ?gloss ^memo:hasPart :manuscript_1 .
  ?gloss memo:cites :text_1
  
}
```

## CQ_1.3
Return all the second-level glosses that are part of `manuscript_1` and that annotate or cite `text_1`.

```
PREFIX : <https://w3id.org/irnerio/data/memo/> 
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/> 

SELECT ?gloss

WHERE {

  ?gloss a memo:Gloss .
  ?gloss ^memo:hasPart :manuscript_1 .
  ?gloss (memo:annotates|memo:cites) / (memo:annotates|memo:cites) :text_1
  
}
```

## CQ_1.4
Return all the second-level glosses that are part of `manuscript_1` and that annotate or refer to `gloss_a`.

```
PREFIX : <https://w3id.org/irnerio/data/memo/>
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/>

SELECT ?gloss

WHERE {

  ?gloss a memo:Gloss .
  ?gloss ^memo:hasPart :manuscript_1 .
  ?gloss (memo:annotates|memo:refersTo) / (memo:annotates|memo:refersTo) :gloss_a
  
}
```

## CQ_1.5
Return all the second-level glosses that annotate or cite `text_1`.

```
PREFIX : <https://w3id.org/irnerio/data/memo/> 
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/> 

SELECT ?gloss

WHERE {

  ?gloss a memo:Gloss .
  ?gloss (memo:annotates|memo:cites) / (memo:annotates|memo:cites) :text_1
  
}
```

## CQ_1.6
Return all the third-level glosses that annotate `gloss_b`.

```
PREFIX : <https://w3id.org/irnerio/data/memo/> 
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/> 

SELECT ?gloss

WHERE {

  ?gloss a memo:Gloss .
  ?gloss memo:annotates / memo:annotates / memo:annotates :gloss_b
  
}
```

## CQ_1.7
Return all the glosses that cite a manuscript.

```
PREFIX : <https://w3id.org/irnerio/data/memo/> 
PREFIX memo: <https://w3id.org/irnerio/ontology/memo/> 

SELECT ?gloss
WHERE {
  ?gloss a memo:Gloss .
  ?manuscript a memo:Manuscript .
  ?gloss memo:cites ?manuscript
}
```
