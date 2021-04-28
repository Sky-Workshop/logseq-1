---
title: upper ontology
---

## Domein invariante ontologie.
## Wikipedia : https://en.wikipedia.org/wiki/Upper_ontology
## Typen: linguistic en realist.
|Linguistic|Realist|Multi|Info objects|
|DOLCE|FBO|DUL|IOLite|
|SUMO|UFO-A, UFO-B|gUFO||
|UFO-C||||
## BOT (Building Ontology) heeft een generalisatie vanuit DUL:
bot:Site rdfs:subClassOf dul:PhysicalPlace .

bot:Zone rdfs:subClassOf dul:PhysicalObject .

bot:Building rdfs:subClassOf dul:DesignedArtifact .
bot:Storey rdfs:subClassOf dul:DesignedArtifact .
bot:Space rdfs:subClassOf dul:DesignedArtifact .
bot:Element rdfs:subClassOf dul:DesignedArtifact .
bot:Interface rdfs:subClassOf dul:DesignedArtifact .

bot:has3DModel rdfs:subPropertyOf dul:hasRegion .
bot:has3DModel rdfs:range dul:SpaceRegion .

bot:containsZone rdfs:subPropertyOf dul:hasPart .
bot:containsElement rdfs:subPropertyOf dul:hasPart .

bot:adjacentZone rdfs:subPropertyOf dul:hasCommonBoundary .
bot:adjacentElement rdfs:subPropertyOf dul:hasCommonBoundary .
bot:interfaceOf rdfs:subPropertyOf dul:hasCommonBoundary .

bot:intersectsZone rdfs:subPropertyOf dul:overlaps .
bot:intersectingElement rdfs:subPropertyOf dul:overlaps .
## DOLCE, Universiteit van Bologna, Aldo Gangemi
##
