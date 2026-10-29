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
3. Kontroller forhåndsvisningen. Bruk sidestørrelse eller «Alle» for å se flere rader.
4. Åpne «Kolonnemapping» hvis du vil endre hvilke Excel-kolonner som kobles til feltene i appen. Kolonner som ikke brukes kan settes til «Ikke brukt».
5. Summeringsrader uten Global ID oppdages og utelates fra aktivitetsimporten. De vises fortsatt i forhåndsvisningen med status.
6. Bekreft importen når valideringen ser riktig ut.

Importen er lokal i nettleseren, men Excel-lesebiblioteket lastes fra en CDN. Derfor trengs internett når Excel-importen brukes første gang.

Beregninger og antakelser
-------------------------
PERT forventet estimat: (O + 4 × ML + P) / 6.
PERT-usikkerhet (standardavvik): (P - O) / 6.
I Excel-importen avrundes forventet arbeidsmengde til hele timer slik arbeidsboken gjør.

Fanen «Antakelser» er valgfri. Hvis den finnes og kan leses, hentes arbeidstid per dag, arbeidsdager per uke, effektivitet og rollekapasiteter derfra. Hvis den mangler, bruker appen synlige standardverdier: 7,5 timer per dag, 5 arbeidsdager per uke og 75 % effektivitet. Manglende kapasitet håndteres med en synlig reserveberegning fra importerte arbeidsdager eller ved å anta én tilgjengelig person. Kontroller slike varsler før du stoler på kalenderdatoer.

Avhengigheter: F betyr slutt–start, P betyr start–start. P-avhengigheter skal ikke behandles som F. LOE-arbeid vises i prosjektet, men skal ikke alene forlenge den kritiske stien.

Prosjektarbeid
--------------
- «Tøm prosjekt» fjerner prosjektets aktiviteter fra visningen etter bekreftelse.
- WBS-grupper kan kollapses og utvides med pilene ved gruppenavnene. Bruk «Kollaps alle» eller «Utvid alle» for hele treet.
- Prosjektet kan lagres lokalt i nettleseren, og prosjektfil kan brukes som sikkerhetskopi.
- Eksportformater kan omfatte prosjektfil (JSON), CSV, Excel, SVG, PNG og PDF, avhengig av visningen/funksjonen.

Merk
----
Dette er en MVP/prototype. Kontroller alltid importforhåndsvisningen, varselmeldinger og beregnede verdier før prosjektplanen brukes som grunnlag for beslutninger. Importen beregner verdier på nytt i applikasjonen; lagrede Excel-formler behandles ikke som fasit.
