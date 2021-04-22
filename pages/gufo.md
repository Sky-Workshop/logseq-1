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
## Hoe verhouden een op gufo gebaseerde ontologie zich tot operationele data?
### Jan de verzorger kan een instantie van gufo:Object zijn
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
## In [[VPH]] kan arbeidsongeschiksheid gemodelleerd worden als een gufo:IntrinsicMode.
#+BEGIN_EXAMPLE
:arbeidsOngeschiktHeid rdf:type owl:Class ;
    rdfs:subClassOf gufo:IntrinsicMode .
:arbeidsOngeschiktHeidVan rdf:type owl:ObjectProperty;
    rdfs:subPropertyOf gufo:inheresIn ;
    rdfs:domain :arbeidsOngeschiktHeid ;
    rdfs:range :Person .
#+END_EXAMPLE
### Een vph:Arbeidsovereenkomst is geen http://purl.org/nemo/gufo#TemporaryRelationshipSituation omdat een Situation een verzameling relaties is en geen verzameling individuals
## subProperties
|subProperty|Property|
|gufo:partitions|gufo:categorizes|
|gufo:isSubCollectionOf|gufo:isObjectProperPartOf|
|gufo:isCollectionMemberOf|gufo:isObjectProperPartOf|
|gufo:isComponentOf|gufo:isObjectProperPartOf|
|gufo:isSubQuantityOf|gufo:isObjectProperPartOf|
|gufo:isAspectProperPartOf|gufo:isProperPartOf|
|gufo:isEventProperPartOf|gufo:isProperPartOf|
|gufo:isObjectProperPartOf|gufo:isProperPartOf|
|gufo:isSituationProperPartOf|gufo:isProperPartOf|
|gufo:standsInQualifiedRelationship|gufo:standsIn|
|gufo:standsInQualifiedParthood|gufo:standsIn|
|gufo:standsInQualifiedInstantiation|gufo:standsIn|
|gufo:standsInQualifiedAttribution|gufo:standsIn|
|gufo:standsInQualifiedConstitution|gufo:standsIn|
## All gUFO ObjectProperties
|
|-------------------------------------|---------------------------------------|---------------------------------------|
| gufo:broughtAbout                   | gufo:Event                            | gufo:Situation                        |
| gufo:concernsConstitutedEndurant    | gufo:TemporaryConstitutionSituation   | gufo:Endurant                         |
| gufo:concernsNonRigidType           | gufo:TemporaryInstantiationSituation  | gufo:NonRigidType                     |
| gufo:concernsQualityType            | gufo:QualityValueAttributionSituation | gufo:EndurantType                     |
| gufo:concernsReifiedQualityValue    | gufo:QualityValueAttributionSituation | gufo:QualityValue                     |
| gufo:concernsRelatedEndurant        | gufo:TemporaryRelationshipSituation   | gufo:Endurant                         |
| gufo:concernsRelationshipType       | gufo:TemporaryRelationshipSituation   | gufo:RelationshipType                 |
| gufo:concernsTemporaryWhole         | gufo:TemporaryParthoodSituation       | gufo:Endurant                         |
| gufo:constitutes                    | gufo:ConcreteIndividual               | gufo:ConcreteIndividual               |
| gufo:contributedToTrigger           | gufo:Situation                        | gufo:Event                            |
| gufo:externallyDependsOn            | gufo:ExtrinsicMode                    | gufo:Endurant                         |
| gufo:hasAssociatedQualityValueType  | gufo:EndurantType                     | gufo:AbstractIndividualType           |
| gufo:hasBeginPoint                  | gufo:ConcreteIndividual               | time:Instant                          |
| gufo:hasEndPoint                    | gufo:ConcreteIndividual               | time:Instant                          |
| gufo:hasReifiedQualityValue         | gufo:ConcreteIndividual               | gufo:QualityValue                     |
| gufo:historicallyDependsOn          | gufo:ConcreteIndividual               | gufo:ConcreteIndividual               |
| gufo:inheresIn                      | gufo:Aspect                           | gufo:ConcreteIndividual               |
| gufo:isAspectProperPartOf           | gufo:Aspect                           | gufo:Aspect                           |
| gufo:isCollectionMemberOf           | gufo:Object                           | gufo:Collection                       |
| gufo:isComponentOf                  | gufo:Object                           | gufo:FunctionalComplex                |
| gufo:isEventProperPartOf            | gufo:Event                            | gufo:Event                            |
| gufo:isObjectProperPartOf           | gufo:Object                           | gufo:Object                           |
| gufo:isProperPartOf                 | owl:Thing                             | owl:Thing                             |
| gufo:isSituationProperPartOf        | gufo:Situation                        | gufo:Situation                        |
| gufo:isSubCollectionOf              | gufo:Collection                       | gufo:Collection                       |
| gufo:isSubQuantityOf                | gufo:Quantity                         | gufo:Quantity                         |
| gufo:manifestedIn                   | gufo:Aspect                           | gufo:Event                            |
| gufo:mediates                       | gufo:Relator                          | gufo:Endurant                         |
| gufo:participatedIn                 | gufo:Object                           | gufo:Event                            |
| gufo:standsIn                       | owl:Thing                             | gufo:Situation                        |
| gufo:standsInQualifiedAttribution   | gufo:Endurant                         | gufo:QualityValueAttributionSituation |
| gufo:standsInQualifiedConstitution  | gufo:Endurant                         | gufo:TemporaryConstitutionSituation   |
| gufo:standsInQualifiedInstantiation | gufo:Endurant                         | gufo:TemporaryInstantiationSituation  |
| gufo:standsInQualifiedParthood      | gufo:Endurant                         | gufo:TemporaryParthoodSituation       |
| gufo:standsInQualifiedRelationship  | gufo:Endurant                         | gufo:TemporaryRelationshipSituation   |
| gufo:wasCreatedIn                   | gufo:Endurant                         | gufo:Event                            |
| gufo:wasTerminatedIn                | gufo:Endurant                         | gufo:Event                            |
| owl:bottomObjectProperty            | owl:Thing                             | owl:Thing                             |
| owl:topObjectProperty               | owl:Thing                             | owl:Thing                             |
##
