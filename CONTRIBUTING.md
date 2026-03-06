# Bidra till OpenSverige (org & agent-infra)

Tack för att du vill bidra. **Osäker var du ska börja?** [Start här](START_HAR.md) — då får du en väg utifrån vad du vill göra.

Vi samarbetar främst via **Discord** ([opensverige.se](https://www.opensverige.se/)); för spårbara ärenden (buggar, features, förändringar i agent-specs) använder vi **GitHub Issues**. Detta dokument beskriver hur vi jobbar tillsammans i denna repo och med agent-strukturen.

---

## Discord eller Issue?

| Använd **Discord** för … | Använd **Issue** för … |
|--------------------------|-------------------------|
| Frågor, diskussion, välkomst | Buggrapporter |
| Snabba beslut, "hur gör jag X?" | Feature requests |
| Allmän community-kontakt | Förändring av agent-spec (memory/tools/identity) |
| | Beslut som ska vara spårbara och länkbara till PR |

**Kort regel:** Vill du bara fråga eller diskutera — kom till [Discord](https://www.opensverige.se/). Vill du att något ska ligga kvar och kunna kopplas till kod/PR — öppna en Issue.

---

## Minimal väg (för nybörjare eller den som bara vill bidra med text)

Du behöver inte kunna Git eller PR. Öppna ett [issue](https://github.com/OPENSVERIGE_ORG/.github/issues) med din idé, förslag eller text, eller skriv i **[Discord](https://www.opensverige.se/)**. Någon från communityt kan hjälpa till att formulera det som en PR om det behövs. Det räcker att beskriva vad du vill ändra eller lägga till.

---

## PR-väg (om du vill göra ändringen själv)

Har du write access till repot? Skapa då en branch. Har du det inte? Forka repot eller fråga i [Discord](https://www.opensverige.se/) så kan någon ge dig access eller skapa en branch åt dig.

1. **Fork eller branch**  
   I org:en kan du oftast skapa en branch direkt i denna repo (`main` → `feature/namn` eller `docs/namn`).

2. **Gör ändringar**  
   - Använd mallar i `agent-infra/*/_template.md` när du lägger till nytt (memory, tool, identity).  
   - Uppdatera README eller AGENT.md om du lägger till nya mappar eller flöden.

3. **Commit**  
   - Meningsfulla commit-meddelanden (t.ex. "feat(identity): add support-agent role" eller "docs(memory): clarify policy format").

4. **Pull Request**  
   - Beskriv *vad* och *varför*.  
   - Länka eventuell issue.  
   - När du ändrar agent-infra eller manifesto, kan en notis skickas till Discord så att andra ser det.

5. **Review & merge**  
   - Någon från org:en (eller du själv enligt policy) reviderar. Efter godkänd review mergas in.

---

## Var ska mitt bidrag ligga?

| Du vill … | Plats |
|-----------|--------|
| Lägga till/ändra minnesdefinition, policy, domänfakta | `agent-infra/memory/` |
| Registrera eller ändra ett verktyg (API, MCP) | `agent-infra/tools/` |
| Lägga till/ändra en agent-identitet (roll, gränser) | `agent-infra/identity/` |
| Ändra principer för hela org:en | `manifesto.md` |
| Förbättra beskrivningar av scaffolden | `AGENT.md`, `README.md`, eller respektive `agent-infra/*/README.md` |
| Ändra workflows (t.ex. Discord) | `workflows/` |
| Föreslå ny funktion eller diskutera | [Discord](https://www.opensverige.se/) (eller öppna en issue om det ska spåras) |

---

## Principer att följa (manifesto)

Alla bidrag ska vara i linje med [manifesto.md](manifesto.md):

- **Transparens** — inga hemliga eller ogenomskinliga delar i specar och definitioner.
- **Öppenhet** — specar och mallar i versionerad, öppen form; datakällor och beroenden angivna där det gäller.
- **Samarbete** — diskussion och tydlighet så att hela org:en kan använda och vidareutveckla strukturen.

Om du är osäker på om en ändring följer manifestot, fråga i PR:en eller i en issue.

---

## Frågor?

- **Discord och alla community-länkar** — [opensverige.se](https://www.opensverige.se/).
- **Issue** — om du vill att ärendet ska vara spårbart: [öppna en issue](https://github.com/OPENSVERIGE_ORG/.github/issues) i denna repo.

*OpenSverige · ett hem där alla kan collaba*
