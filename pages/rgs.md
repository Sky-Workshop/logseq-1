---
title: RGS
---

## Vraag van Marc om voor Tijn de concepten rekening schema, rubriek, rekening in VPH op te nemen.
## Representatie is niet belangrijk; dit zou ook het probleem van het weergeven van een tabel openbaren.
## RGS "entry points" legt de relatie tussen ../presentation/rgs-hierarchie-pre.xml" en "../dictionary/rgs-mapping_jaarverantwoording-2020-nlgaap-stichtingen.xm". De vraag is welke rekening types voor de verpleeghuizen (zorg) van toepassing zijn.
- rgs:EntryPoint
- rgs:
## rekeningen-lab-nl.xml bevat rekening labels
## rekeningen.xml bevat de rekeningnummers
## rekeningen-ref.xsd bevat de rekeningnummers
## Pseudo code om van xml naar rdf te komen:
- lees
- lees rekeningen-ref.xml ref:Number b.v. 0101010.01
- haal label op via xlink:label="rgs-i_BIvaKouVvpBeg_ref" uit rekeningngen-ref.xsd
-
