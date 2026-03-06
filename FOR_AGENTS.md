# För AI-agenter — OpenSverige

Denna fil är för AI-agenter som arbetar i OpenSverige-org eller denna repo. Läs den som kontext så att du följer våra regler och struktur.

---

## Regler (obligatoriska)

- **Följ [manifesto.md](manifesto.md):** Transparens, öppenhet. Inga API-nycklar, tokens eller hemligheter i repot. Specar och mallar i `agent-infra/`; implementation och credentials sätts lokalt av användaren.
- **Specar och mallar** hör hemma i `agent-infra/`. Använd `_template.md` i varje mapp vid nya definitioner.

## Struktur (referens)

| Sökväg | Innehåll |
|--------|----------|
| `agent-infra/memory/` | Minne, policy, domänfakta |
| `agent-infra/tools/` | Verktyg/API-specar (endast spec, inga nycklar) |
| `agent-infra/identity/` | Roller och gränser per agent |

## Vad agenten aldrig får göra

- Committa nycklar, tokens eller hemligheter.
- Ignorera manifesto-principerna (transparens, öppenhet).

## Vid bidrag

- Ändringar via PR som följer [CONTRIBUTING.md](CONTRIBUTING.md).
- Vid osäkerhet: föreslå ändring utan att committa känslig data.
