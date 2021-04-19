---
title: RGS
---

## Vraag van Marc om voor Tijn de concepten rekening schema, rubriek, rekening in VPH op te nemen:
- RGS maar gebruik van RGS-code voor xlink waardes, b.v. rgs-i_BIva_loc 
- RGS kent een role met een roleURI naar b.v. kvk, bzk en frc
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
## Daarnaast zijn twee role’s toegevoegd voor de definitie van respectievelijk de RGS-code (from_dts) en een concept uit een entrypoint (to_dts). DTS is een XBRL concept en staat voor Discoverable Taxonomy Set.
## Software die RGS aan kan staat op [rgsready.nl. De essentie is dat RGS codes gebruikt worden.
## TODO Welke RGS codes zijn relevant voor
:PROPERTIES:
:todo: 1618836432084
:END:
