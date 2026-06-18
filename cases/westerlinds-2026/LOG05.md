# Ärendelogg: H 434-26 (Hyresnämnden)

## 2026-06-18 — Incident & Digital komplettering

### Incidentbeskrivning
Vid efterkontroll av det postade bevismaterialet (Volym 2) upptäcktes ett kritiskt formateringsfel i huvuddokumentet `00_HUVUDDOKUMENT_Tidslinje_och_bevisindex.pdf`. 

* **Orsak:** WYSIWYG-renderingsmotorn i MarkText misslyckades med att hantera tabellmarginalerna vid PDF-export. Det resulterade i att tabellens högra kolumn ("Kritisk observation & sökväg för mappar och filer") blev horisontellt avklippt vid utskrift.
* **Inverkan:** Delar av filsökvägarna och de tekniska kommentarerna blev oläsliga i den tryckta/exporterade versionen. Det underliggande materialet på USB-minnena var helt opåverkat.

### Åtgärd
1. Källkodsfilen (`tidslinje_05Y.md`) migrerades tillbaka till VS Code för korrekt hantering av radbrytning (`word-wrap`).
2. Ny, fullständig PDF genererades under filnamnet: `00_HUVUDDOKUMENT_Tidslinje_och_bevisindex_2026.06.18.pdf`.
3. Digital komplettering skickades via e-post till Hyresnämnden i Sundsvall (kl. 13:46) med begäran om att filen ska läggas till i ärendets akt.
4. Dokumentets kryptografiska integritet säkrades genom att inkludera SHA-256-hashsträngen direkt i e-postmeddelandet för verifiering mot framtida manipulation.

### Fil- och hash-specifikation
```text
40ecda2237e3bc4beaa0c3b380d53ecb91c2d588ac4b90006069918f2fe1eec5  00_HUVUDDOKUMENT_Tidslinje_och_bevisindex_2026.06.18.pdf
