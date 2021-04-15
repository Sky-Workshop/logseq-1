---
title: Business en vestiging onderscheid
---

## Zie ook [[R Seegers]]
## kik:Vestiging
  ```rdf:type owl:Class ;
  rdfs:isDefinedBy <https://www.kvk.nl> ;
  rdfs:label "Vestiging"@nl ;
  rdfs:subClassOf kik:Verblijfsobject ;
  rdfs:subClassOf [
      rdf:type owl:Restriction ;
      owl:onClass vph:Business ;
      owl:onProperty vph:partOf ;
      owl:qualifiedCardinality "1"^^xsd:nonNegativeInteger ;
    ] ;
  rdfs:subClassOf [
      rdf:type owl:Restriction ;
      owl:onDataRange xsd:string ;
      owl:onProperty vph:heeftVestigingsNummer ;
      owl:qualifiedCardinality "1"^^xsd:nonNegativeInteger ;
    ] ;
  <http://www.w3.org/2004/02/skos/core#definition> "Een gebouw of complex van gebouwen waar duurzame uitoefening van de activiteiten van een onderneming of rechtspersoon plaatsvindt."@nl ;
  vph:definitionSource "Kamer van Koophandel"@nl ;
. ```
##
