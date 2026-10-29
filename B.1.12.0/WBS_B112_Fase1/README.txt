WBS PLANLEGGER – B.1.12 (FASE 1)
=================================

ÅPNE APPEN
Dobbeltklikk index.html. Appen er en enkeltstående HTML-fil.
Du trenger ikke server eller konto. Excel-import kan kreve internett
for å hente det eksterne Excel-lesebiblioteket.

NYTT I FASE 1
- Ressursregister for personer, utstyr/systemer og andre ressurser.
- Rolle og tilgjengelighet (%) per ressurs.
- Flere ressurser kan knyttes til hver arbeidspakke.
- Ansvarlig person/rolle (eksisterende felt), nå med forslag fra registeret.
- Status: Ikke startet, Pågår, Blokkert, Fullført.
- Planlagt kapasitet (%) og effektivitetsfaktor (%) på arbeidspakken.
- Risiko: sannsynlighet 1–5, konsekvens 1–5, beskrivelse og tiltak.
- Risikoscore og status vises i WBS-tabellen.
- Nye felt følger med ved JSON-eksport/import. De fleste nye felt
  er også med i vanlig CSV- og Excel-eksport.
- Eldre JSON-prosjekter uten de nye feltene kan fortsatt åpnes.

VIKTIG OM BEREGNINGER
Planlagt kapasitet og effektivitetsfaktor i de NYE feltene er
foreløpig kun informasjonsfelter. De endrer IKKE PERT, kritisk sti
eller Gantt. Eksisterende Excel-import har egne kapasitets- og
effektivitetsverdier som brukes i beregningen. Disse er bevart
og må ikke forveksles med de nye planleggingsfeltene.

RISIKO
Score = sannsynlighet x konsekvens (1–25). Lav: 1–6,
moderat: 7–14, høy: 15–25. Dette er eksempelgrenser,
ikke en universell standard. Risiko påvirker ikke varigheten.

KOMPATIBILITET OG SIKKERHET
- Ta alltid en JSON-sikkerhetskopi av et eksisterende prosjekt
  før du åpner det i en ny appversjon.
- Ressursregisteret og de nye feltene er med i JSON-prosjektfilen.
- Eksport i originalt Excel-estimeringsformat beholder originalens
  kolonner og inneholder IKKE alle de nye planleggingsfeltene.
- Prosjektet lagres lokalt i nettleseren. Ulike nettlesere eller
  filstier kan ha separate lagringsområder.
- B.1.11.2 fra den innleverte versjonen er ikke overskrevet.

TESTET
- Nettlesertest av registrering, endring og visning av ressurs,
  ansvarlig, kapasitet, effektivitet, status og risiko.
- JSON-eksport og import med nye felt.
- Åpning av eldre JSON-fil uten de nye feltene.
- CSV-nedlasting og JavaScript-syntaks.
- Ingen rapporterte JavaScript-feil i disse testene.

IKKE IMPLEMENTERT ENNÅ (SENERE FASER)
- Ressursutjevning, faktisk kapasitetsberegning og automatisk
  justering av PERT/Gantt.
- Bedre zoom, sticky redigeringspanel, masseeksport,
  WBS-hierarkidiagram, forbedret linjeføring og prosjektoversikt.
