WBS Planlegger – MVP med Excel-import

Slik starter du
1. Pakk ut ZIP-filen.
2. Åpne index.html i en moderne nettleser (Chrome eller Edge anbefales).
3. Prosjektet starter tomt. Bruk «Last eksempelprosjekt» dersom du vil utforske appen med eksempeldata.
4. Velg «Importer Excel» for å laste opp en arbeidsbok.

Excel-import
- Importveiviseren er inspirert av Power BI: velg fil, velg ark, velg header-rad, kontroller forhåndsvisning og valideringsmeldinger, og bekreft deretter importen.
- Forventet mal er et ark med kolonnene fra «Estimering». Appen leter først etter dette arket automatisk.
- Appen leser antakelser fra «Antakelser» når arket finnes; ellers brukes standardverdier og brukeren advares.
- Beregningene kjøres på nytt i appen ut fra O, ML og P, ikke fra lagrede Excel-resultater.
- PERT-estimat = avrundet (O + 4 × ML + P) / 6.
- PERT-usikkerhet sigma = (P − O) / 6.
- Arbeidstimer = avrundet PERT-estimat / effektivitet.
- Arbeidsdager = arbeidstimer / (kapasitet × arbeidstimer per dag).
- F-avhengighet tolkes som finish-to-start; P-avhengighet tolkes som start-to-start.
- LOE-aktiviteter vises parallelt med prosjektet, men påvirker ikke kritisk sti.
- Global ID benyttes for å koble avhengigheter. Importøren støtter lokale ID-er, Global ID-er og kjente intervalluttrykk i avhengighetskolonnen.
- Før bekreftelse vises antall rader, ugyldige estimater, dupliserte Global ID-er og eventuelle avhengigheter som ikke kan kobles sikkert.
- Importen erstatter prosjektet som er åpent. Appen ber om bekreftelse dersom prosjektet ikke er tomt.

Andre funksjoner
- WBS-hierarki med grupper, arbeidspakker og milepæler.
- Kritisk-sti-diagram med ES, DR, EF, LS, TF og LF, WBS-gruppefarger og kritiske piler.
- Redigerbare aktiviteter og avhengigheter, med FS/SS-type.
- Gantt-diagram med arbeidsdager mandag–fredag.
- Lokal lagring, JSON-prosjektfil, CSV, Excel, SVG/PNG og utskrift/Lagre som PDF.
- Excel-prosjekter får i tillegg en «Excel-data»-visning med de 21 opprinnelige kolonnene.

Viktig
- Excel-lesing bruker SheetJS fra CDN ved første import. Det krever internettforbindelse første gang importfunksjonen brukes.
- Prosjektet lagres lokalt i nettleseren og følger ikke automatisk med til en annen PC. Eksporter en JSON-prosjektfil som sikkerhetskopi.
- Appen er en prototype. Kontroller resultatene mot kjente testeksempler før bruk i viktige prosjektbeslutninger.
