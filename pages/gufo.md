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
## Hoe verhouden een op gufo gebaseerde ontologie zich tot operationele data?
### Jan de verzorger kan een instantie van gufo:Object
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
### Subclasses
### instances
### subclasses types
### instances
### subclasses types
### instances of types
