# Agent-scaffold — OpenSverige GitHub Org

Detta dokument beskriver **hur agent-strukturen är uppbyggd** och var du hittar vad. Det är vår gemensamma scaffold så att alla i org:en kan arbeta konsekvent med agenter.

---

## Struktur (org-nivå)

```
.github/                    ← denna repo (org:s hem)
├── README.md               ← org-profil + välkomst
├── manifesto.md            ← principer (transparens, öppenhet, samarbete)
├── AGENT.md                ← denna fil
├── CONTRIBUTING.md         ← hur man bidrar
├── agent-infra/            ← gemensam agent-scaffold
│   ├── memory/             ← minne: vad agenten får komma ihåg
│   │   ├── README.md       ← definition + regler
│   │   └── _template.md    ← mall för nya minnesdefinitioner
│   ├── tools/              ← verktyg: API:er, MCP, skript
│   │   ├── README.md
│   │   └── _template.md
│   └── identity/           ← identitet: roller och gränser per agent
│       ├── README.md
│       └── _template.md
├── workflows/              ← GitHub Actions (t.ex. Discord-sync)
└── .github/                ← issue- och PR-mallar
    ├── ISSUE_TEMPLATE/
    └── PULL_REQUEST_TEMPLATE.md
```

**Andra repon** i org:en kan:
- Länka hit för specifikationer och mallar
- Ha egen implementation (Cursor rules, skills, MCP) som **följer** dessa specar
- Referera till [manifesto.md](manifesto.md) i sin egen dokumentation

**API-nycklar:** Denna repo innehåller endast specar och mallar. Inga API-nycklar eller hemligheter får committas. Kör du agenten lokalt (t.ex. klonat repo på Mac mini) sätter du egna nycklar i miljövariabler eller `.env` (som inte följer med i repo). Se [manifesto](manifesto.md) och [SECURITY](SECURITY.md).

---

## Så här jobbar vi tillsammans

| Roll / behov | Var du jobbar | Flöde |
|--------------|----------------|-------|
| **Lägga till nytt minne** (t.ex. policy, domänfakta) | `agent-infra/memory/` | Ny fil (eller kopia av `_template.md`) → PR → review |
| **Registrera nytt verktyg** (API, MCP, script) | `agent-infra/tools/` | Ny spec enligt mall → PR → review |
| **Definiera ny agent eller uppdatera roll** | `agent-infra/identity/` | Ny/uppdaterad identitetsfil → PR → review |
| **Ändra principer** | `manifesto.md` | PR med tydlig motivering → bred review |
| **Förbättra scaffold** (ny mapp, ny mall) | Root / `agent-infra/` | Issue först (valfritt), sedan PR |

När någon pushar eller öppnar PR som rör `agent-infra/**` (eller `agent-specs/**`) kan en workflow skicka notis till Discord så att andra hinner följa med.

---

## För implementatörer (andra repon)

- **Cursor / IDE:** Använd `agent-infra/identity/` för att veta vilka roller och gränser som gäller; inkludera manifesto-länk i rules/skills.
- **MCP / API:** Verktyg som exponeras för agenter bör ha en motsvarande spec under `agent-infra/tools/` med datakälla och öppenhetskrav.
- **Memory / state:** Om agenten sparar långvarigt minne, beskriv format och policy i `agent-infra/memory/` så att det stämmer med manifesto (transparens, öppenhet).

---

## Snabblänkar

- **AI-agenter:** Se [FOR_AGENTS.md](FOR_AGENTS.md) för samlade regler och struktur som kontext.
- [Manifesto](manifesto.md)
- [Memory – README](agent-infra/memory/README.md)
- [Tools – README](agent-infra/tools/README.md)
- [Identity – README](agent-infra/identity/README.md)
- [CONTRIBUTING](CONTRIBUTING.md)

---

*OpenSverige · agent-scaffold för hela org:en*
