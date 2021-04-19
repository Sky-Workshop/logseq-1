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
## Uit het handboek informatie zorgverzekeringswet U kunt de jaarrekening op 2 manieren opstellen:
    u gebruikt een modeljaarrekening van het CIBG;
    u gebruikt een eigen model jaarrekening of dat van uw administratiekantoor of accountantskantoor.
