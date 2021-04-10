---
title: Gufo
---

## Characteristics:
### Supports instantiation  ans specialization of gufo individuals ans classes
### Is a taxonomy of individuals
#### instantiates gufo classes, e.g. :Earth rdf:type gufo:Object
#### specializes gufo classes , e.g. :SoccerMatch rdfs:subClassOf gufo:Event
### Is a taxonomy of types
#### instantiations of gufo types, e.g. :Planet rdf:type gufo:Kind
#### specializes gufo types, e.g. :PersonPhase rdfs:subClassOf gufo:Phase
### Vaak worden specialisaties van een gufo class gecombineerd met instantie van een gufo type. b.v. `
        :Person rdf:type owl:Class ;
            rdfs:subClassOf gufo:Object ;
            rdf:type gufo:Kind .
###
###
## Hoe verhouden een op gufo gebaseerde ontologie zich tot operationele data?
### Jan de verzorger kan een instantie van gufo:Object
## Direct gebruikmaken van de gufo classes geeft al snel richting aan semantiek
## Individual
### AbstractIndividual
### ConcreteIndividual
#### Endurant
##### Object
##### Aspect
#### Event
#### Situation
## Type
### AbstractIndividualType
    ConcreteIndividualType
        EndurantType
            Sortal
                Kind
                Phase
                Role
                SubKind
            NonSortal
                Category
                PhaseMixin
                RoleMixin
                Mixin
        EventType
        SituationType
    RelationshipType
## In VPH kan arbeidsongeschiksheid gemodelleerd worden als een gufo:IntrinsicMode.
#+BEGIN_QUOTE
:arbeidsOngeschiktHeid rdf:type owl:Class ;
    rdfs:subClassOf gufo:IntrinsicMode .
:arbeidsOngeschiktHeidVan rdf:type owl:ObjectProperty;
    rdfs:subPropertyOf gufo:inheresIn ;
    rdfs:domain :arbeidsOngeschiktHeid ;
    rdfs:range :Person .
#+END_QUOTE
##
