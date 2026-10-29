# B.1.17.1 – UX-forbedringer (fase 5)

Åpne `index.html` direkte i nettleseren. Prosjektdata lagres lokalt i nettleseren, akkurat som i forrige versjon. Eksporter gjerne prosjektet som JSON før du tester.

Endringer:
- Sammenleggbar prosjektinnstillingslinje, med kompakt prosjektsammendrag når lukket.
- WBS: `Vis kolonner` med Standard/Planlegging/Alle og individuelle avkrysningsbokser. Valget lagres lokalt for UI; ingen data fjernes, og eksport er uendret.
- Diagramverktøylinjene har en mer ensartet utforming. Ingen endringer i PERT, Gantt eller kritisk-sti-motoren.
- Sticky handlingsknapper nederst i redigeringspanelet.
- Oppmerksomhetspunkter viser alvorlighetsgrad og beholder direkte navigasjon til aktivitetene.
- Lagringsstatus tydeliggjør at dataene lagres i *nettleseren*, ikke automatisk som en ekstern prosjektfil.

Test spesielt:
1. Åpne/lukk Prosjektinnstillinger; rediger navn og startdato.
2. Bytt kolonneprofil og enkeltkolonner i WBS, rull horisontalt og prøv med importert Excel.
3. Rediger og lagre en aktivitet mens redigeringspanelet er scrollet.
4. Åpne varsler og naviger til aktivitet; test Gantt og kritisk sti.
5. Eksporter og importer prosjekt som JSON; kontroller at prosjektdata er bevart.
