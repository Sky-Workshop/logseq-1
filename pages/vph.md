---
title: VPH
---

## [[Decubitus]] zou volgens [[ICD-11]] gemodelleerd kunnen worden https://icd.who.int/browse11/l-m/en#/http%3a%2f%2fid.who.int%2ficd%2fentity%2f455330172.
### Een valide waarde is dan /http://id.who.int/icd/entity/380028323, zie https://icd.who.int/browse11/l-m/en#/http://id.who.int/icd/entity/380028323 .
### De resteert dan waar deze class in [[VPH]] wordt opgenomen.
## Momenteel is VPH een herbouw van een combinatie van classes uit DOLCE, gUFO, BFO etc Relaties zijn gedefinieerd maar nog niet toegekend aan domein classes.
## Alleen object properties:
heeftHuisnummer	NummerAanduiding
heeftHuisnummerToevoeging	NummerAanduiding
heeftPostcode	NummerAanduiding
heeftVerzuimPeriode	WerkOvereenkomst
is_client_binnen_verpleegproces	VPH-domain-ontology:Human

is_client_binnen_verpleegproces	NursingProcess
hasAgreement	VPH-domain-ontology:Agreement
hasDescription	VPH-domain-ontology:Description
bijbehorendeOpenbareRuimte	VPH-domain-ontology:PublicArea
hasQuality	VPH-domain-ontology:Quality
hasQualityValue	VPH-domain-ontology:QualityValue
hasUnitOfMeasure	VPH-domain-ontology:UnitOfMeasure
bijbehorendeWoonplaats	VPH-domain-ontology:VillageOrCity
heeftVerzuimPeriode	VerzuimPeriode
## en datatype properties:
