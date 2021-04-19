---
title: RGS
---

## Vraag van Marc om voor Tijn de concepten rekening schema, rubriek, rekening in VPH op te nemen:
- RGS maar gebruik van RGS-code voor xlink waardes, b.v. rgs-i_BIva_loc. Deze begin kennelijk altijd met rgs-i_ ; derhalve rgs-i_<code>
- rgs-i_<code>_loc is een locator (verwijzing naar een externe file)
- RGS kent een role met een roleURI naar b.v. kvk, bzk en frc
- Het lijkt dat RGS geen concept voor rubriek te kennen. 
- RGS maakt onderscheid tussen de rekeningen structuur en de presentatie die gebruik maakt van een relatie en een volgorde nummer.
![2021_04_19_afbeelding.png](https://cdn.logseq.com/%2F8f1ae382-5f18-4f77-89b5-10a6cfda69c5342cd70c-45d4-4844-b82d-79ebdc6e6af72021_04_19_afbeelding.png?Expires=4772437427&Signature=X1Sj3bTHNzmLjHXU0~AH9UEkyQlPDq1RUiCpLZl6Luzmrmr8fz2K9T3xxur-zxnFA5KDW53dfnkYef6oWg2gVG39jPFi3nBW5JCkSS~5knRavaJA2f6uuIUDNIrSdI0NWqinJNUpc15o0567tietXwyAPzP3arDK6P21EMdIA9H3ZrfWrL~Ch3SxATldvPvBQ9JkAlugN4lcGZnUmYFNA6GVTiWPy~xDadJlyz7TNNCwLhLab4yZghciFtuSj-HzQ7tt5KzBsvhO~hEHZdeBfh3~24RywE9pVEmGmLlmNLb-x6hdZzfHwDXpMBEy-jzcbIzmt-lvOvhTtgpSyszZmw__&Key-Pair-Id=APKAJE5CCD6X7MP6PTEA)
## Ook https://cure4.nl/publicatie/blog-nieuw-rekeningschema/ geeft een algemeen geldend rekeningschema maar dan specifiek voor de zorg.
## Het laagste niveau lijken rubrieken met een 4 karakter RGScode rgs-i_ABCD
## Representatie is niet belangrijk; dit zou ook het probleem van het weergeven van een tabel openbaren.
## RGS "entry points" legt de relatie tussen ../presentation/rgs-hierarchie-pre.xml" en "../dictionary/rgs-mapping_jaarverantwoording-2020-nlgaap-stichtingen.xm". De vraag is welke rekening types voor de verpleeghuizen (zorg) van toepassing zijn.
- rgs:EntryPoint
- rgs:
## rekeningen-lab-nl.xml bevat rekening labels
## rekeningen.xml bevat de rekeningnummers
## rekeningen-ref.xsd bevat de rekeningnummers
## Rekening nummers zijn of 99 of 9999999 of 9999999.99
## Pseudo code om van xml naar rdf te komen:
- lees uit rekeningen-ref.xml relaties tussen rekening nummer en label via link:referenceArc xlink:type="arc"
- lees uit deze relatie ref:Number b.v. 0101010.01
- haal label op via xlink:label="rgs-i_BIvaKouVvpBeg_ref" uit rekeningngen-ref.xsd
## Daarnaast zijn twee role’s toegevoegd voor de definitie van respectievelijk de RGS-code (from_dts) en een concept uit een entrypoint (to_dts). DTS is een XBRL concept en staat voor Discoverable Taxonomy Set.
## Software die RGS aan kan staat op [rgsready.nl](https://www.softwarepakketten.nl/cmm/swp/raadplegen_eigenschappen_kort.php?slt=72&bronw=1). De essentie is dat RGS codes gebruikt worden.
## TODO Welke RGS-codes zijn relevant voor ZiN?
:PROPERTIES:
:todo: 1618836432084
:END:
## Uit het handboek informatie zorgverzekeringswet (Zvw) :U kunt de jaarrekening op 2 manieren opstellen:
    1. u gebruikt een modeljaarrekening van het CIBG; https://www.jaarverantwoordingzorg.nl/?utm_source=jaarverslagenzorg.nl&utm_medium=redirect&utm_campaign=redirect
    2. u gebruikt een eigen model jaarrekening of dat van uw administratiekantoor of accountantskantoor.
Gebruik van RGS zou dan dus invulling van optie 2 zijn.
## TODO Is er een verschil in financiële verslaglegging naar openbare bronnen en naar b.v. NzA? Dit kan zo zijn en moet dus gemodelleerd worden. We kennen dus de openbare jaarverantwoording en de aanvrager specifieke jaarverantwoording. Ik vermoed dat financiële cijfers nooit openbaar zijn.
:PROPERTIES:
:todo: 1618840319004
:END:
## Kleinere organisaties kunnen een micro status krijgen waarbij er andere verantwoordingsregels gelden. In VPH/KIK moet dus deze status gemodelleerd worden.
## In DigiMV worden de volgende VVT variabelen gerapporteerd:
Tabblad	Variable	Position	Label
x9conc_total_1	Q_TypeVvtFinanciering_Ans_TypeVvtFinanciering#1	40	Indien Verpleging, verzorging en thuiszorg - financiering: Zvw en/of Wlz
x9conc_total_1	Q_TypeVvtFinanciering_Ans_TypeVvtFinanciering#2	41	Indien Verpleging, verzorging en thuiszorg - financiering: Zorg gefinancierd uit de Jeugdwet
x9conc_total_24	qPersVvtSpecOud_AantalPers	5103	Specialist ouderengeneeskunde/basisarts - Aantal werkzame personen op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecOud_AantalFte	5104	Specialist ouderengeneeskunde/basisarts - Aantal fte's op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecPsycho_AantalPers	5105	(GZ-)Psycholoog - Aantal werkzame personen op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecPsycho_AantalFte	5106	(GZ-)Psycholoog - Aantal fte's op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVplSpec_AantalPers	5107	Verpleegkundig specialist - Aantal werkzame personen op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVplSpec_AantalFte	5108	Verpleegkundig specialist - Aantal fte's op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVplHbo_AantalPers	5109	Verpleegkundige hbo - Aantal werkzame personen op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVplHbo_AantalFte	5110	Verpleegkundige hbo - Aantal fte's op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVplMbo_AantalPers	5111	Verpleegkundige mbo - Aantal werkzame personen op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVplMbo_AantalFte	5112	Verpleegkundige mbo - Aantal fte's op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVzIG_AantalPers	5113	IG-Verzorgende - Aantal werkzame personen op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVzIG_AantalFte	5114	IG-Verzorgende - Aantal fte's op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVzHlp_AantalPers	5115	Verzorgende/helpende - Aantal werkzame personen op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecVzHlp_AantalFte	5116	Verzorgende/helpende - Aantal fte's op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecZorghlp_AantalPers	5117	Zorghulp - Aantal werkzame personen op 31 december van verslagjaar
x9conc_total_24	qPersVvtSpecZorghlp_AantalFte	5118	Zorghulp - Aantal fte's op 31 december van verslagjaar
## Modelleer keuzes:
### Concepten:
#### namespace nt15: <http://www.nltaxonomie.nl/rgs/nt15/rgs/20201117.b/dictionary/rekeningen>
#### Grootboekschema aka rekeningstelseltr
    vph:RekeningStelsel 
        rdfs:subClassOf ... ;
        rdfs:label "Rekeningstelsel"@nl ;
        rdfs:label "General ledger"@en ;
        skos:definition "General ledger system according governance guidelines."@en
        skos:definition "Standaard rekening stelsel volgens rijksoverheid standaard."@nl
#### Grootboekrekening 
    vph:GrootboekRekening 
        rdfs:subClassOf ... ;
        rdfs:label "Grootboekrekening"@nl ;
        rdfs:label "Ledger account"@en ;
        nt15:hasRGSCode nt15:hasRGSCode .
#### RGS code
    nt15:RGSCode
        rdfs:subClassOf ... ;
        rdfs:label "RGS code"@nl ;
        rdfs:label "RGS code"@en .
#### Grootboekrekeningnaam
    vph:GrootboekRekeningNaam 
        rdfs:subClassOf ... ;
        rdfs:label "Grootboekrekeningnaam"@nl ;
        rdfs:label "Ledger account name"@en .
#### Grootboekrekeningnummer
    vph:GrootboekRekeningNummer 
        rdfs:subClassOf ... ;
        rdfs:label "Grootboekrekeningnummer"@nl ;
        rdfs:label "Ledger account number"@en .
#### Rekening telt rekening samen
    nt15:steltRekeningSamen 
        rdfs:subPropertyOf ... ; 
        rdfs:label "Is deel van rekening"@nl ;
        rdfs:label "Comprises ledger account"@en ;
        rdfs:domain
####
