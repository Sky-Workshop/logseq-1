---
title: RGS
---

## Vraag van Marc om voor Tijn de concepten rekening schema, rubriek, rekening in VPH op te nemen:
- RGS maar gebruik van RGS-code, b.v. 
- Het lijkt dat RGS geen concept voor rubriek kent. 
- RGS maakt onderscheid tussen de rekeningen structuur en de presentatie die gebruik maakt van een relatie en een volgorde nummer.
## Representatie is niet belangrijk; dit zou ook het probleem van het weergeven van een tabel openbaren.
## RGS "entry points" legt de relatie tussen ../presentation/rgs-hierarchie-pre.xml" en "../dictionary/rgs-mapping_jaarverantwoording-2020-nlgaap-stichtingen.xm". De vraag is welke rekening types voor de verpleeghuizen (zorg) van toepassing zijn.
- rgs:EntryPoint
- rgs:
## rekeningen-lab-nl.xml bevat rekening labels
## rekeningen.xml bevat de rekeningnummers
## rekeningen-ref.xsd bevat de rekeningnummers
## Pseudo code om van xml naar rdf te komen:
- lees uit rekeningen-ref.xml relaties tussen rekening nummer en label via link:referenceArc xlink:type="arc"
- lees uit deze relatie ref:Number b.v. 0101010.01
- haal label op via xlink:label="rgs-i_BIvaKouVvpBeg_ref" uit rekeningngen-ref.xsd
