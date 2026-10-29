WBS PLANLEGGER – MVP
====================

Start
-----
1. Pakk ut ZIP-filen.
2. Åpne wbs-mvp/index.html i Chrome eller Edge.
3. Appen starter med et tomt prosjekt.

Excel-import
------------
1. Trykk «Importer Excel» og velg arbeidsboken.
2. Velg ark og header-rad i importvinduet.
3. Kontroller forhåndsvisningen. Du kan vise 12, 25, 50, 100 eller alle rader.
4. Kjente kolonnenavn kobles automatisk. Ikke-gjenkjente kolonner foreslås utelatt og vises grå.
5. Bruk «Koble felt» eller «Endre felt» direkte i kolonneoverskriften dersom du trenger å endre en kobling. Bare én feltvelger åpnes om gangen.
6. Bruk «Utelat» / «Ta med» ved kolonner som er koblet til et importfelt.
7. Summeringsrader uten Global ID oppdages og utelates fra aktivitetsimporten.
8. Bekreft importen når valideringen ser riktig ut. Importvinduet lukkes etter vellykket import.

Importen er lokal i nettleseren, men Excel-lesebiblioteket lastes fra en CDN. Derfor trengs internett når Excel-importen brukes.

Beregninger og antakelser
-------------------------
PERT forventet estimat: (O + 4 × ML + P) / 6.
PERT-usikkerhet (standardavvik): (P - O) / 6.
I Excel-importen avrundes forventet arbeidsmengde til hele timer slik arbeidsboken gjør.

Fanen «Antakelser» er valgfri. Hvis den finnes og kan leses, hentes arbeidstid per dag, arbeidsdager per uke, effektivitet og rollekapasiteter derfra. Hvis den mangler, bruker appen synlige standardverdier. Manglende kapasitet håndteres med en reserveberegning fra importerte arbeidsdager eller ved å anta én tilgjengelig person; kontroller varslene før du stoler på kalenderdatoene.

Avhengigheter: F betyr slutt–start, P betyr start–start. LOE-arbeid vises i prosjektet, men skal ikke alene forlenge den kritiske stien.

Diagrammer og WBS
-----------------
- Kritisk sti og Gantt kan filtreres på hele prosjektet, en WBS-gruppe eller en enkelt aktivitet/milepæl.
- Bruk + / − / 100 % for å zoome i diagrammene.
- Dra bokser i kritisk-sti-diagrammet for å flytte dem. «Fordel bokser» lager et nytt automatisk oppsett for valgt visning.
- De røde stiplede forbindelsene i Gantt viser overgangene langs kritisk sti.
- WBS-grupper kan kollapses med pilen ved gruppenavnet. Bruk «Kollaps alle grupper» eller «Utvid alle grupper» for hele treet.
- Eksempelbiblioteket har fire små prosjekter: nettside, fagdag, analyserapport og flytting.

Lagring og eksport
------------------
Prosjektet lagres lokalt i nettleseren. Eksporter en JSON-prosjektfil som sikkerhetskopi før du rydder eller bytter prosjekt. Eksport av CSV, Excel, SVG, PNG og PDF er tilgjengelig fra relevante visninger/eksportfanen.

Merk
----
Dette er en MVP/prototype. Kontroller alltid importforhåndsvisningen, varselmeldinger og beregnede verdier før prosjektplanen brukes som beslutningsgrunnlag. Importen beregner verdier på nytt i applikasjonen; lagrede Excel-formler behandles ikke som fasit.

Utseende
--------
Klikk «Utseende» øverst for å velge mellom seks fargetemaer: Nordisk, Ocean Glass, Skog, Lavendel, Sand og Mørk modus. Velg også bakgrunn: Enkel, Himmelblå, Mint, Solnedgang eller Tropisk by. Du kan dessuten laste opp et eget bakgrunnsbilde; det skaleres ned i nettleseren og lagres lokalt.

Du kan justere tekststørrelse, tetthet/avstand, panelenes opasitet og bakgrunnens synlighet. Innstillingene lagres separat fra prosjektet i den aktuelle nettleseren. Eget bakgrunnsbilde følger derfor ikke automatisk med hvis prosjektet åpnes på en annen enhet; velg bildet på nytt der. Den innebygde «Tropisk by»-bakgrunnen følger med HTML-filen.
