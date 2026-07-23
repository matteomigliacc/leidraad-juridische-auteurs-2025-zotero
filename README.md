# Leidraad Juridische Auteurs 2025 voor Zotero

> Verwijs volgens de [**Leidraad voor juridische auteurs**](https://shop.wolterskluwer.nl/Leidraad-voor-juridische-auteurs-sNPLEIJUAU/), elfde druk (Deventer 2025), met [Zotero](https://www.zotero.org).

Dit is een vakantieproject geweest. Ik werk al jaren met Zotero om jurisprudentie, literatuur en rapporten en kamerstukken in op te slaan die ik wil gebruiken in mijn voetnoten etc. Daarvoor maakte ik voorheen altijd gebruik van de CSL-stijl van van **Joël Hendriks** en **Pieter van der Wees** (zie uitgebreid [(hieronder)](#met-dank-aan)), alleen met de nieuwe Leidraad en de mogelijkheden om met een taalmodel dit allemaal wat aan te vullen ben ik in de vakantie aan de slag gegaan. Dit leverde het volgende op: drie CSL-stijlen die het complete verwijssysteem van de Leidraad pogen te implementeren: literatuur, Nederlandse en Europese rechtspraak, regelgeving en parlementaire
stukken. Het is getoetst tegen de voorbeelden uit de Leidraad zelf en gevalideerd tegen
het officiële CSL 1.0.2-schema van Zotero. 


> **NB: Best effort, geen keurmerk.** Deze stijlen komen enorm in de buurt maar zijn zeker niet perfect. De Leidraad is
> dik en lang niet alles kan mooi in een CSL worden gevat. Een paar gevallen pakken daarom net anders uit, en
> een enkele keuze is een gemotiveerde eigen invulling. Zie
> [Best effort: waar het niet 100% is](#best-effort-waar-het-niet-100-is), en
> controleer bij twijfel je verwijzing en de eisen van je uitgever.

---

## Inhoud

NB : Dit is automatisch gegenereerd door Claude Code. 

- [Welke stijl kies je?](#welke-stijl-kies-je)
- [Installeren in Zotero](#installeren-in-zotero)
- [Bronnen invoeren](#bronnen-invoeren) — literatuur, rechtspraak, regelgeving, Kamerstukken, online
- [Wat de stijl dekt](#wat-de-stijl-dekt)
- [Best effort: waar het niet 100% is](#best-effort-waar-het-niet-100-is)
- [Met dank aan](#met-dank-aan)
- [Licentie](#licentie)

---

## Welke stijl kies je?

De Leidraad kent één aanbevolen methode en een alternatief (bijlage B), en
tijdschriften citeren weer net anders omdat ze geen literatuurlijst hebben.
Vandaar drie bestanden:

| bestand | methode | literatuurlijst |
|---|---|---|
| **`leidraad-2025.csl`** | de aanbevolen methode: verkort verwijzen met `auteur + jaartal` | ja |
| **`leidraad-2025-bijlage-b.csl`** | de variant uit bijlage B: verkort met de **verkorte titel** erbij | ja |
| **`leidraad-2025-tijdschrift.csl`** | de **volledige** methode: eerste keer voluit, daarna verkort | nee |

Wat het verschil in de praktijk betekent:

| | aanbevolen | bijlage B | tijdschrift |
|---|---|---|---|
| eerste verwijzing | `Van Opijnen 2014, par. 2.1.` | `Van Opijnen, Op en in het web 2014/2.1.` | `M. van Opijnen, Op en in het web…, Den Haag: Boom juridisch 2014, par. 2.1.` |
| latere verwijzing | idem (steeds kort) | idem (steeds kort) | `Van Opijnen, Op en in het web 2014/2.1.` |
| lijst achterin | ja | ja | — |

- **Aanbevolen** — de standaard voor de meeste boeken, scripties en dissertaties:
  een korte voetnoot (`auteur + jaartal`) plus een literatuurlijst achterin.
- **Bijlage B** — hetzelfde, maar de korte verwijzing draagt óók de verkorte
  titel. Sommige uitgevers en redacties schrijven dit voor; de Leidraad beveelt
  het zelf aan wanneer een werk niet met `auteur + jaartal` te onderscheiden is
  (p. 149). Overleg met je uitgever of eindredacteur.
- **Tijdschrift** — voor publicaties zonder literatuurlijst. Een literatuurbron
  staat de eerste keer voluit in de voetnoot en elke latere keer verkort. Zie
  [De tijdschriftmethode](#de-tijdschriftmethode).

Jurisprudentie en regelgeving zien er in alle drie de stijlen hetzelfde uit.

---

## Installeren in Zotero

1. Download het gewenste `.csl`-bestand (of alle drie) van de **Releases**-pagina.
2. Open Zotero → **Instellingen** (of *Preferences*) → tabblad **Citeren** →
   sectie **Stijlen**.
3. Klik op **➕ Stijl toevoegen uit bestand…** en kies het `.csl`-bestand.
   (Alternatief: dubbelklik het bestand; Zotero biedt aan het te installeren.)
4. In je tekstverwerker (Word, LibreOffice, Google Docs via de connector) kies je
   de stijl in de documentinstellingen — hij heet daar *Leidraad voor juridische
   auteurs 2025* (met tussen haakjes `bijlage B` of `tijdschrift` voor de varianten).

Dat is alles. Verwijzingen en de literatuurlijst worden vanaf dan volgens de
Leidraad opgemaakt.

> **Waarom de invoer ertoe doet.** Zotero heeft geen velden voor een ECLI, een
> vergaderjaar of een Kamerstuknummer. Een stijlbestand is nooit beter dan de
> gegevens die het krijgt, dus leg de sectie hieronder vast welk Zotero-veld welk
> Leidraad-element draagt. Zonder die conventie werken vooral rechtspraak en
> regelgeving niet goed.

---

## Bronnen invoeren

Waar hieronder **Extra** staat, bedoelen we het Zotero-veld *Extra* met een regel
in de vorm `cslvariabele: waarde`; Zotero zet die om in een echte CSL-variabele.

### Boek

| Zotero-veld | Inhoud |
|---|---|
| Item Type | Book |
| Author | voorletters + achternaam; tussenvoegsel in het aparte deel van het naamveld |
| Title | volledige titel, met hoofdletter |
| Place / Publisher / Date | plaats · uitgever · jaartal |
| Series / Series Number | reeksnaam en deelnummer, als die er zijn |
| Extra | `genre: diss. Amsterdam UvA` of `genre: oratie Leiden` |

> Voetnoot: `Van Opijnen 2014, par. 2.1.`
> Lijst: **Van Opijnen 2014** — M. van Opijnen, *Op en in het web…* (diss. Amsterdam UvA), Den Haag: Boom juridisch 2014.

**Auteurloos werk.** Laat Author leeg en vul **Short Title** met de verkorte
titel die als opschrift dient. De Leidraad (p. 35-36) laat de keuze tussen
verkorte titel en institutionele auteur; pas die keuze consequent toe.

> `UWV ontslagprocedure 2016, p. 33-34.`

### Bijdrage in een bundel

| Zotero-veld | Inhoud |
|---|---|
| Item Type | Book Section |
| Author | auteur van de **bijdrage** |
| Title | titel van de bijdrage (komt tussen ‘ ’) |
| Book Title | titel van de bundel (cursief) |
| Editor | redacteur(en) — wordt automatisch `(red.)` |
| Place / Publisher / Date / Pages | als bij een boek, plus begin- en eindpagina |

> Lijst: **Koekkoek 2024** — B. Koekkoek, ‘Van “verwarde personen” naar onbegrepen gedrag…’, in: E.R. Muller, N. Kop & E.J. van der Torre (red.), *Politie. Organisatie en functioneren van de politie in Nederland*, Deventer: Wolters Kluwer 2024, p. 289-306.

> Gebruik het veld **Editor**, niet Book Author. Book Author is voor een bundel
> waarvan één auteur het hele boek schreef.

### Tijdschriftartikel

| Zotero-veld | Inhoud |
|---|---|
| Item Type | Journal Article |
| Publication | tijdschrifttitel, afgekort volgens hoofdstuk 6 van de Leidraad |
| Issue | **publicatienummer** — de `686` in `NJB 2022/686` |
| Pages / Date | begin- en eindpagina · jaartal |

Geen publicatienummer? Laat Issue leeg. Begint de paginering **per aflevering**
opnieuw, zet dan het afleveringsnummer in Extra als `number: 6/7` (niet in Issue):
`Openbaar bestuur 1998, afl. 6/7, p. 32-33.`

> Lijst: **Vroege 2022** — B. Vroege, ‘De EU als wapenleverancier…’, *NJB* 2022/686, p. 808-814.

### De tijdschriftmethode

Met `leidraad-2025-tijdschrift.csl` verandert de **veldinvoer niet** — alleen de
voetnoot gedraagt zich anders: een literatuurbron staat de **eerste keer voluit**
en **daarna verkort**.

> ¹ A. Dirksen, ‘Een artikel in het NJB’, *NJB* 2025/536, par. 5.
> ⁷ Dirksen, *NJB* 2025/536, par. 5.

De verkorte vorm leunt op **Short Title**: vul die in bij werken die je vaker
aanhaalt, anders valt hij terug op de volledige titel. Verwijs je naar een
**paragraaf** van een boek of handboek, dan hangt dat nummer als schuine streep
achter het jaartal — in beide vormen (`Asser/Sieburgh 6-III 2022/13`); een
**pagina** krijgt de gewone `, p. 73`. Deze methode geldt alleen voor literatuur;
jurisprudentie en regelgeving haal je elke keer volledig aan.

### Boekbespreking (§2.4.3)

Gaat het om **het besproken boek**, dan volgt na de titel `(bespreking van: …)`.
Item Type *Journal Article*, met in Extra:

```
reviewed-author: Diamant || M.
reviewed-title: Het budgetrecht van het Nederlandse parlement…
reviewed-genre: (diss. Leiden), Deventer: Wolters Kluwer 2017
```

CSL kan geen bron ín een bron beschrijven: uitgever en jaar van het besproken werk
gaan daarom in `reviewed-genre`. Gaat het om **de bespreking als geheel**, dan
volstaat `genre: boekbespreking` en laat je de `reviewed-`velden leeg.

### Interview (§2.4.4)

De geïnterviewde staat vooraan; de interviewers volgen na `in:`.

| Zotero-veld | Inhoud | Wordt |
|---|---|---|
| Item Type | Interview | |
| Interviewee | Van Ettekoven, B.J. | `Van Ettekoven 2021` |
| Interviewer | Boersema, W.; Kleinnijenhuis, J. | `in: W. Boersema & J. Kleinnijenhuis` |
| Publication / Date | Trouw · 20 november 2021 | cursief · volledige datum |
| Extra | `genre: interview met B.J. van Ettekoven, voorzitter ABRvS` | `(interview met …)` |

### Jurisprudentie

| Zotero-veld | Inhoud |
|---|---|
| Item Type | Case |
| Court | instantie, **al afgekort**: `HR`, `ABRvS (grote kamer)`, `Rb. Zeeland-West-Brabant (ktr.)` |
| Date Decided | volledige datum — wordt `7 juni 2024` |
| Docket Number | de ECLI; bij EU-zaken zaaknummer én ECLI: `C-477/17, ECLI:EU:C:2019:60` |
| Case Name | roepnaam — cursief tussen haakjes aan het eind |
| History | toevoeging tussen haakjes **vóór** de vindplaats: `concl. A-G J. Spier` |
| Reporter / Reporter Volume | vindplaats (cursief) en nummer: `NJ` · `2016/173` |
| Extra | toevoeging **ná** de vindplaats: `m.nt. T. Hartlief`, `m.red.aant.` |

> **History staat vóór de vindplaats, Extra erachter.** Vandaar `concl.` in
> History en `m.nt.` in Extra.

**Nederlandse rechtspraak (§4.4.1).** Het Court-veld draagt de afgekorte
instantienaam met plaats- of gebiedsnaam. De ECLI-code vertelt welke:

| ECLI-code | Court |
|---|---|
| `RBAMS`, `RBDHA`, … | `Rb. ` + plaatsnaam (`Rb. Amsterdam`) |
| `GHARL`, `GHAMS`, … | `Hof ` + plaatsnaam (`Hof Arnhem-Leeuwarden`) |
| `HR` / `RVS` / `CRVB` / `CBB` | `HR` / `ABRvS` / `CRvB` / `CBb` |

Een verbijzondering hoort erachter tussen haakjes: `ABRvS (grote kamer)`.

> `Rb. Gelderland 7 juni 2024, ECLI:NL:RBGEL:2024:3636, r.o. 5.7.`

**HvJ EU en Gerecht EU (§4.5).** Zaaknummer **én** ECLI, door een komma
gescheiden, samen in Docket Number:

> `HvJ EU 24 januari 2019, C-477/17, ECLI:EU:C:2019:60, BNB 2019/66, m.nt. P. Kavelaars (Baladin).`

Gebruik `Gerecht EU`, `HvJ EG` of `GvA EU` in Court naar gelang instantie en
periode. Gevoegde zaken zet je vóór de nummers in Docket Number:
`gevoegde zaken C-793/19 en C-794/19, ECLI:EU:C:2020:791`.

**EHRM (§4.6).** Géén apart zaaknummer — de ECLI bevat aan het einde al het
applicatienummer (p. 100). Docket Number bevat dus alleen de ECLI. Vul Case Name
altijd met de roepnaam (klager `/` verwerende staat):

> `EHRM 24 november 2005, ECLI:CE:ECHR:2005:1124JUD005388600, NJ 2006/250, m.nt. J.A. Peters (Tourancheau/Frankrijk).`

**Conclusie A-G als bron.** Zet de hele aanduiding in Court, inclusief `Concl.` en
de naam mét voorletters (Leidraad p. 96); de PHR-ECLI in Docket Number:

> `Concl. A-G J. Spier 20 november 2015, ECLI:NL:PHR:2015:2307, par. 7.1 (McDonald-van Biezen/McDonald en Delta Lloyd).`

**Rechtsoverweging of paragraaf.** De keuze tussen `r.o.` en `par.` hangt aan hoe
de uitspraak zelf zijn onderdelen nummert, niet aan de instantie. Kies bij het
invoegen de locatorsoort:

| Locatorsoort | Resultaat | Wanneer |
|---|---|---|
| Paragraph | `r.o. 3.8` | rechtsoverwegingen — Nederlandse rechters, HvJ EU |
| Section | `par. 58` | genummerde paragrafen — EHRM, conclusies A-G |
| Page | `p. 334` | geen genummerde onderdelen |

**Meerdere vindplaatsen.** Reporter draagt er één; zijn het er meer, laat Reporter
dan leeg en zet de hele reeks in Extra (de tijdschrifttitels verliezen daar wel hun
cursivering — CSL kan geen opmaak in een vrij tekstveld aanbrengen).

### Regelgeving

| Zotero-veld | Inhoud |
|---|---|
| Item Type | Statute |
| Name of Act | de citeertitel; leeg als de regeling er geen heeft |
| Code | publicatieblad, cursief: `Stb.`, `Stcrt.`, `Trb.`, `Gemeenteblad` |
| Date Enacted / Public Law Number | jaartal · bladnummer |

Mét citeertitel komt de vindplaats tussen haakjes; zonder staat zij op zichzelf:

> `Besluit vergoeding reorganisatiekosten politie (Stb. 1993, 216).`
> `Gemeenteblad 2025, 127502.`

### Kamerstukken, Handelingen en Kamervragen

| Zotero-veld | Inhoud |
|---|---|
| Item Type | Bill |
| Code | `Kamerstukken II`, `Kamerstukken I`, `Handelingen II`, `Aanhangsel Handelingen II` — cursief |
| Session | vergaderjaar: `2015/16` |
| Bill Number | dossiernummer: `34442` |
| Section | documentnummer |

Het veld Section: staat er alleen een getal, dan komt er `nr. ` voor (`3` → `nr. 3`);
staat er iets anders (`A`, `nr. 23, item 14`), dan wordt het letterlijk overgenomen.
De pagina is een **locator**, geen veld: `…, nr. 3, p. 7.`

### Frequent geactualiseerde uitgaven (§2.6.3)

Groene Serie, Vakstudie, Sdu Commentaar, Tekst & Commentaar — werken die online
staan en doorlopend worden bijgewerkt. Die krijgen geen jaartal maar de laatste
bijwerkdatum. Item Type *Book Section*, Date **leeg**, en in Extra:

```
container-title-short: GS Onrechtmatige daad
available-date: 2024-02-28
```

> `Oldenhuis, in: GS Onrechtmatige daad, art. 6:164 BW, aant. 4.2 (online, bijgewerkt 28 februari 2024).`

De aanduiding (`art. 6:164 BW, aant. 4.2`) typ je voluit in het locatorveld; kies
als soort *Pagina* — de stijl laat het label bij deze werken weg.

### Online bronnen

| Bron | Item Type | Webadres |
|---|---|---|
| Blog | Blog Post | Blog Title (`cassatieblog.nl`) |
| Webpagina, nieuwsbericht | Web Page | Website Title (`nu.nl`) |
| Video | Video Recording | Studio = kanaal, Place = `youtube.com` |
| Podcast | Podcast | Publisher = organisatie |

Vul Date met de **volledige** datum. Mét auteur krijgt de bron een verkorte
verwijzing (`Tanja 2025.`); zonder auteur wordt de voetnoot voluit
(`‘Wat is open access?’, openaccess.nl.`).

### Besluiten van toezichthouders

Een boete, besluit of richtsnoer van een toezichthouder krijgt geen eigen vorm:
voer het in als een gewoon **Report** met de **autoriteit in het auteursveld**
(als één-veld-naam via het schakelaartje naast het naamveld). Zet in de titel wat
het is; de datum volledig.

> `UODO 14 maart 2024, Boete (Szpital Południowy w Warszawie).`

---

## Wat de stijl dekt

| Bronsoort | Leidraad |
|---|---|
| Boeken, incl. reeks, dissertatie, oratie | §2.3.1, §2.3.7 |
| Bijdragen in bundels | §2.3.3 |
| Tijdschriftartikelen, met publicatienummer | §2.4.1 |
| Boekbesprekingen, interviews | §2.4.3, §2.4.4 |
| Auteurloze werken, jaarsuffix `2016a`/`2016b` | p. 35-36, §2.2.1 |
| Nederlandse rechtspraak, met en zonder ECLI | §4.4 |
| HvJ EU, Gerecht EU, EHRM | §4.5, §4.6 |
| Regelgeving, met en zonder citeertitel | §3.2 |
| Kamerstukken I en II, Handelingen, Aanhangsel | §3.4 |
| Frequent geactualiseerde uitgaven, online | §2.6.3 |
| Blogs, webpagina's, podcasts, video's | §2.7 |

Conform §5.1 kent de stijl geen `ibidem`, `a.w.`, `o.c.` of `idem`: de verkorte
verwijzing wordt telkens herhaald, zoals de Leidraad voorschrijft.

## Best effort: waar het niet 100% is

Deze stijlen zijn vrij compleet maar zeker niet perfect, het is en blijft een **best effort**, geen garantie. Een
deel van de Leidraad laat zich niet volledig in CSL vangen, en een paar gevallen
zijn een gemotiveerde eigen keuze. Hier wat van die punten : 

**Door CSL afgedwongen — kan niet anders:**

1. **Eén gecombineerde lijst.** CSL kan per stijl maar één bibliografie maken. De
   lijst is gegroepeerd. Daarom heb ik gekozen om niet alleen literatuur op nemen maar:  literatuur, regelgeving, parlementaire stukken, jurisprudentie, overige online bronnen. Dit dus in plaats van de aparte lijsten van
   §4.8. Alleen de literatuurgroep krijgt het vetgedrukte opschrift. Liever teveel en wat wegknippen dan het helemaal niet krijgen was hier de gedachte. 
2. **Jurisprudentie alfabetisch per instantie**, niet in de territoriaal-hiërarchische volgorde van §4.8: CSL kan de inhoud van een veld niet vergelijken. Dus dat moet je zelf dan nog aanpassen helaas. 
3. **Auteurloze online bronnen** staan tóch in de lijst (achteraan, eigen groep); CSL kan een geciteerd item niet uit de bibliografie weglaten. Verwijder ze met de hand als je de Leidraad strikt volgt.
4. **Instantie- en tijdschriftafkortingen** typ je zelf in het Court- of
   Publication-veld: hoofdstuk 6 bevat een lijst van honderden afkortingen die niet
   in een stijlbestand past.

**Kleine oneffenheden:**

- **Internationaal Gerechtshof.** De stijl zet Case Name altijd tussen haakjes; de
  Leidraad doet dat bij het IGH juist niet, dus krijg je dubbele haakjes. Zet de
  zaaknaam voor IGH-uitspraken in Extra in plaats van Case Name — dan staat hij
  goed (maar niet cursief).
- **Annotatie als zelfstandige bron.** De voetnoot klopt; in de literatuurlijst
  zet de stijl er aanhalingstekens omheen (`‘annotatie bij …’`) die de Leidraad
  daar niet gebruikt (p. 97). Cosmetisch, en alleen in de lijst.
- **Meerdere vindplaatsen in Extra** verliezen hun cursivering — CSL kan geen
  opmaak aanbrengen binnen een vrij tekstveld.

**Eigen keuzes waar de Leidraad zwijgt:**

- Gevoegde EU-zaken, de conclusie van de A-G bij het HvJ EU, en de afkorting `GiA`
  voor het Gerecht in ambtenarenzaken (naar analogie van `GiEA`) staan niet als
  voorschrift in de Leidraad. Ze zijn met reden gekozen; wijkt jouw vakgebied af,
  houd dan je eigen gewoonte aan.

Wat de stijl sowieso niet oplost: verwijzingen naar wetsartikelen (`art. 6:162 BW`)
horen volgens §3.3 in de lopende tekst, niet in een literatuurbeheerder.

**Kortom:** controleer bij twijfel je verwijzing tegen de Leidraad, en volg de
eisen van je uitgever of eindredacteur. Zie je een fout of afwijking? Meld het door een Issue te openen, dan maken we hem samen alleen maar beter. 

---

## Met dank aan

Deze stijlen voor de druk van 2025 zijn opnieuw opgebouwd, met een testharnas dat
elke verwijzing toetst tegen de voorbeelden in de Leidraad. Ik heb dit zeker niet met de hand gedaan, maar grotendeels Claude Code aangestuurd; het was een leuk vakantieproject.  

Dit hele project was er niet geweest zonder het prachtige handwerk van **Joël Hendriks** en **Pieter van der Wees**, die de eerste
Leidraad-stijl voor Zotero maakten (editie 2019). Zonder dat pionierswerk was ik hier niet op gekomen om verder uit te werken, en had ik al die jaren ook zonder gezeten. Veel dank dus naar Joël en Pieter. 

## Licentie

Creative Commons **Attribution-ShareAlike 3.0** (CC BY-SA 3.0), in lijn met de
oorspronkelijke stijl. Je mag de bestanden gebruiken, aanpassen en delen, mits met
naamsvermelding en onder dezelfde licentie.
