---
title: Onderbouwing gebruik ORG
---

## Wat kan kik-v gebruiken van de ORG ontologie
## De ontologie wordt door andere gebruikt  ![2021_04_13_afbeelding.png](https://cdn.logseq.com/%2F8f1ae382-5f18-4f77-89b5-10a6cfda69c551ece5de-0e34-4eac-aaef-14e4c6a2be3b2021_04_13_afbeelding.png?Expires=4771925875&Signature=Ock0msjDluIyhZdHQKJO9Vbq6TKMx74t79iMe59zSDaTYzUU-~lmAUTjDtNn4uy40m5vMFTGKdC3KXjzb6h4VWzzQiOxrOwdgBv3mjnFyjAkuhXTjfwYVIRvvPWh0zpJA7B3xJZbMVzS~lwveM9QTR2HvIzhj2rtbLxHmwromysDipw5bym4zjCAsu4kJkgL4hMYCHWc6SY4vXthyJ0qWLho09A~engUnby4flUvL9qE2oVB66OzPWFjEF85VQsYZqgVQ9pC9mgAKL~mLz~wRcKcOZGgQRKTrwTf0oZgj~l5gsdu13QgTQ8ZezBQ~oOT2MuYJOFpDfxI~UkG~v5TIg__&Key-Pair-Id=APKAJE5CCD6X7MP6PTEA){:height 283, :width 626}
## Momenteel zijn er een aantal classes in VPH waarvan je kan zeggen dat deze over de organisaties gaan omdat de organisatie over uitvoering gaat:
### [[[[vph:]][[Organization]]]]
### vph:OrganizationalChangeEvent
### vph:IntentionalProcess
## [[[[vph:]][[Organization]]]] en [[ [[vph:]][[OrganizationalChangeEvent]]]] worden ook door ORG ingevuld.
## [[[[vph:]][[IntentionalProcess]]]] zit niet in ORG. Het concept Process wordt veelvuldig gebruikt maar het lastig hier nu al iets van vast te leggen.
## Proces categorieen zijn: Zorgverlening, Calamiteitafhandeling, Data management
## De organisatie ontwikkeling is belangrijk aspect waarvoor meestal PROV wordt gebruikt. 
Zonder deze opvraagbare historie zal er waardevolle gegevens verloren gaan.
### ![2021_04_13_afbeelding.png](https://cdn.logseq.com/%2F8f1ae382-5f18-4f77-89b5-10a6cfda69c51864279a-cf86-4924-a080-fa006359f4bf2021_04_13_afbeelding.png?Expires=4771926351&Signature=EiKjI-DG6KIzcdXhrpMUK91tLEYjmM2kKdAhVdLbbwwwAtrHSXL5oQZJOsWVxT89RpZ6EKLb1p0OQYbO7lsAleRTsWUf8WG38AbK6Lii0u6SXp4MQIkIZoBVj-oi8r8qYtxEtgwQzgMPiMp2V3x6KZWa4gcu~NJ-8F3Qw4-rHan2duCnYHjIN-t0waR-LkZpAKObD2fZbdpjZ9ykIwflGuVYwU~-OXNmQYzH0rgoXFPfLgF3UrrZqRfzldWO-vhJYOFhNQP5o9lP-DTtlemSJbfh~BcjYfheyEetzkLf57gP8pGyfo9uSfTzktvq0KM-JXljc2nLx~WdVAU5aww3YA__&Key-Pair-Id=APKAJE5CCD6X7MP6PTEA)
### [[PROV]][[https://www.w3.org/TR/prov-o/]] gebruikt: Agent, Entity en Activity.
### [[[[prov:]][[Activity]]]] het type van wijzigingen die traceerbaar moet zijn, 
b.v. ontstaan van een zorglocatie.
### In ORG is org:ChangeEvent een subclass van prov:Activity. 
Hiermee kunnen we van oude naar nieuwe organisatie gaan middels SPARQL queries.
## [Hier](https://www.w3.org/2011/gld/wiki/ORG_Validation_Suite) kan het gebruik van ORG worden gecheckt.
## Hoe verder? Een voorstel
### Identificeer classes die
