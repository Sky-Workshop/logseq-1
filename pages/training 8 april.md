---
title: Training 8 april
---

## Training script 8 april 2021

Analyseer structuur:
- Lijst
- Visueel



Met TOP2.ttl open


SELECT *
WHERE {
    ?subject skos:scopeNote gwsw:_NLCS .
}

Analyse en data kwaliteit:

SELECT *
WHERE {
    ?subject ?property gwsw:_NLCS .
}

Voordeel van deze methode?
- Overzicht
- Toont eventuele issues omdat het allemaal skos:scopenotes moeten zijn.
##
