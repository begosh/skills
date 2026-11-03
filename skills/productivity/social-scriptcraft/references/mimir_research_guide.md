# Mímir Research Integration Guide för Video-Manus

När ett video-manus kräver hårda fakta, statistik, historiska exempel eller teknisk precision, kopplas **Mímir** in som researchmotor innan manusförfattandet påbörjas.

---

## 1. Hur Mímir Anropas

Använd den Mímir-skill eller det researchverktyg som är tillgängligt i den aktiva miljön och följ dess aktuella instruktioner. Utgå exempelvis från denna researchfråga:

```text
Forska fram överraskande statistik, historiska exempel och vetenskapliga studier kring [ÄMNE]. Fokusera på konkreta siffror lämpliga för en video-hook. Ange primärkällor, exakta avsnitt och osäkerheter för varje påstående.
```

### Leverans och omfattning:
* Spara rapporten i `./artifacts/research_<namn>.md` om användaren inte valt en annan leveransplats.
* Rikta research mot relevanta primärkällor; ange relevanta domäner och tidsperiod i uppdraget.
* Anpassa omfattningen efter videons behov. Använd bara CLI-flaggor som den installerade versionen faktiskt dokumenterar.
* Om Mímir saknas används tillgängliga sökverktyg. Om inga researchverktyg finns används användarens källor och kvarstående luckor redovisas.

---

## 2. Vad vi ber Mímir om för manus

För att få användbart manusmaterial instrueras Mímir att extrahera:
1. **Statistiska anomalier:** Siffror som bryter sunt förnuft (perfekt för sek 0–3 hooks).
2. **Historiska analogier:** Korta berättelser om kända personer eller händelser (perfekt för akt 2/story).
3. **Teknisk precision / Definitioner:** Korrekta termer och arkitekturdetaljer för att bygga auktoritet.
4. **Vanliga motargument:** Vad skeptiker kommer att kommentera, så att vi kan bemöta det proaktivt i videon.

---

## 3. Hur Research omvandlas till Manus

I manusets tvåkolumns A/V-tabell integreras Mímir-resultaten så här. Exemplet nedan är en mall, inte ett verifierat forskningsresultat; ersätt både siffra och referens med kontrollerade belägg före leverans:

| Tid (Sek) | Ljud / Tal (A-Roll) | Bild / A/V-Regi (B-Roll & Grafik) | Källa / Mímir Ref |
| :--- | :--- | :--- | :--- |
| **00:15 - 00:22** | *"Enligt en studie publicerad i Science ökar retentionen med 68% när..."* | **GRAPHIC:** Stapeldiagram animeras fram med källangivelse i nedre vänstra hörnet. SFX: Swish. | `MÍMIR-SCIENCE-2024-REF` |

Genom att knyta varje påstående till en referens undviks generiska eller felaktiga påståenden, vilket dramatiskt ökar tittarens förtroende och videons retention.
