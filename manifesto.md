# OpenSverige — Manifesto

Detta är våra principer för hur vi bygger och underhåller vår gemensamma agent-infrastruktur. Alla som bidrar eller använder våra agenter förväntas följa dessa värderingar.

---

## Transparens

- **Specifikationer är öppna.** Agenters beteende, minne, verktyg och identitet ska kunna granskas av alla. Inga "svarta lådor".
- **Beslut är spårbara.** Ändringar i agent-specs, policyer och minne ska vara versionerade och motiverade (t.ex. via commit-meddelanden och PR-beskrivningar).
- **Ansvar är tydligt.** Varje agent har en definierad roll och gränser; användare ska veta vem de interagerar med och vilka principer som gäller.

## Öppenhet

- **Kod och spec i öppna repon.** Definitioner, mallar och (där det är möjligt) implementation ska ligga i versionerad, öppen form — inte enbart i binära caches eller hemliga miljöer.
- **Datakällor och beroenden är angivna.** Verktyg och API:er ska dokumentera var data kommer ifrån och under vilken licens/användning det sker.
- **Inga API-nycklar eller hemligheter i repot.** Denna repo innehåller endast specar, mallar och konfiguration. Varje instans (t.ex. klonad och körande på egen maskin 24/7) använder **egna nycklar** som sätts lokalt — miljövariabler, `.env` som inte följer med i repo, eller motsvarande.
- **Samarbete är inbjudet.** Denna struktur är ett hem för hela org:en; alla som vill förbättra agenterna är välkomna att bidra enligt [CONTRIBUTING](CONTRIBUTING.md).

## Samarbete

- **Gemensamt ägande.** Agent-infrastrukturen tillhör organisationen. Vi bygger tillsammans, reviderar tillsammans och håller varandra ansvariga mot detta manifesto.
- **Diskussion före beslut.** Stora förändringar i identity, memory eller tools diskuteras (t.ex. via issues eller PR) så att alla som vill hinner syna och påverka.
- **Enkel onboarding.** Nya medarbetare ska kunna förstå var saker finns och hur man bidrar — därav tydlig mappstruktur, mallar och [AGENT.md](AGENT.md).

---

## Snabbreferens

| Om du vill …              | Gå hit / gör så här …                          |
|---------------------------|------------------------------------------------|
| Läsa vad agenten får minnas | [agent-infra/memory/](agent-infra/memory/)     |
| Definiera eller läsa verktyg | [agent-infra/tools/](agent-infra/tools/)    |
| Se roller och gränser     | [agent-infra/identity/](agent-infra/identity/) |
| Bidra med förändringar    | [CONTRIBUTING.md](CONTRIBUTING.md)             |
| Förstå hela scaffolden    | [AGENT.md](AGENT.md)                           |

---

*Senast uppdaterad: 2025 — OpenSverige*
