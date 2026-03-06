# OpenSverige

**Välkommen till vårt gemensamma hem på GitHub.**

Här i org:en bygger vi tillsammans — och denna repo (`.github`) är **navet** för hur vi jobbar: community health, standarder och **agent-infrastrukturen** som vi alla använder och utvecklar.

---

## Vad finns här?

**Ny eller osäker?** [Start här](START_HAR.md) — då får du en väg utifrån vad du vill göra. **AI-agenter** som jobbar i denna repo: läs [FOR_AGENTS.md](FOR_AGENTS.md) för regler och struktur.

- **[Manifesto](manifesto.md)** — våra principer om transparens, öppenhet och samarbete. Alla agenter och specifikationer ska följa dem.
- **[AGENT.md](AGENT.md)** — översikt över agent-scaffolden: memory, tools, identity och hur vi arbetar tillsammans med dem.
- **`agent-infra/`** — gemensam struktur för agenter:
  - `memory/` — vad agenten får komma ihåg (mallar och definitioner)
  - `tools/` — verktyg och API:er (specar och mallar)
  - `identity/` — roller och gränser per agent
- **`workflows/`** — t.ex. Discord-notiser när agent-specs uppdateras.
- **[CONTRIBUTING.md](CONTRIBUTING.md)** — hur du bidrar med förändringar och diskuterar förbättringar.

**Första projektet:** Vi bygger en bra AI-agent för vår Discord — [discord-agent](https://github.com/opensverige/discord-agent). Eget repo; bygg och pusha fritt (invit till org → [Discord](https://www.opensverige.se/)).

**Kör själv:** Agent-strukturen är öppen så att communityt kan använda och bygga vidare. Klona och kör på egen maskin (t.ex. Mac mini 24/7) med **egna API-nycklar** — inga nycklar, tokens eller hemligheter committas i detta repo.

Om du är ny: börja med [START_HAR.md](START_HAR.md), [manifesto.md](manifesto.md) och [AGENT.md](AGENT.md). Vill du ändra eller utöka strukturen — [Discord](https://www.opensverige.se/) eller öppna en issue/PR.

---

## Så här collabar vi

Vi sitter inte i silos — agent-strukturen är **org-gemensam**. **Discord är vår huvudsakliga kanal** för samarbete och frågor.

- **Discord och alla community-länkar:** [opensverige.se](https://www.opensverige.se/) — gå med, hitta IRL-sessioner, läs manifestet.

Det betyder:

1. **Specar och mallar** ligger här så att alla repon och team kan återanvända dem.
2. **Förändringar** görs via branches och PR; då triggas notiser till Discord så att andra hinner syna.
3. **Stora beslut** (nya agent-roller, nya policyer) diskuteras öppet — i Discord eller i Issues/PR.

**Var ska jag vända mig?** Frågor och diskussion → **Discord**. Bugg, feature eller förändring av agent-spec som ska spåras och länkas till kod → **GitHub Issue**.

Har du frågor eller förslag? Kom till [opensverige.se](https://www.opensverige.se/) (Discord och övrigt) eller öppna en [issue](https://github.com/OPENSVERIGE_ORG/.github/issues) om det ska bli spårbart.

---

*OpenSverige · ett hem där alla kan collaba*
