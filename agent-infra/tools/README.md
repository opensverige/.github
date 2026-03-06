# Tools — OpenSverige Agent-Infrastruktur

Hur vi definierar och dokumenterar **verktyg** (tools) för våra agenter i OpenSverige.

## Syfte

Tools är de färdigheter agenten anropar: API:er, MCP-servrar, skript, datakällor. Varje tool ska ha en tydlig spec som visar **vad den gör**, **vilka data den använder** och **hur den följer våra principer**.

## Definition för OpenSverige

- **Format**: En `.md`- eller spec-fil per tool (eller per tool-grupp) med namn, beskrivning, I/O och policy-koppling.
- **Placering**: `agent-infra/tools/` — specifikationer och mallar; implementation kan ligga i andra repon men ska länkas här.
- **Innehåll**:
  - **Namn och syfte**: Vad verktyget heter och varför det finns.
  - **Input/Output**: Vilka parametrar och vilken typ av data som går in/ut.
  - **Datakälla och licens**: Var data kommer ifrån och under vilken licens (öppenhet).
  - **Säkerhet och integritet**: Ingen känslig data i loggar eller caches utan tydlig policy. **Implementation och credentials sker utanför denna repo** — tool-specen beskriver endast vad verktyget gör och vilka typer av credentials som behövs (API-nyckel, OAuth, etc.), utan att inkludera dem. Varje körning använder egna nycklar (t.ex. miljövariabler).

## Mall för ett tool

```markdown
# [Tool-namn]

## Syfte
En mening om vad verktyget gör och för vilken agent/use-case.

## Input
- `param1` (typ): beskrivning
- `param2` (typ): beskrivning

## Output
Beskrivning av returvärde eller sidoeffekter.

## Datakälla / API
- Källa: [URL eller namn]
- Licens: [t.ex. öppen data, CC, etc.]

## Öppenhet & transparens
- [ ] Spec är public och versionerad
- [ ] Inga hemliga env-variabler utan dokumentation
- [ ] Loggning av anrop (om någon) är policy-konsekvent
```

## Credentials (inga i repot)

Tool-specar i denna mapp beskriver **vad** verktyget gör och **vilka typer** av credentials som krävs (t.ex. "API-nyckel för tjänst X"). Själva nycklar och implementation lägger du till lokalt när du kör agenten — aldrig i detta repo. Se [manifesto](../../manifesto.md).

## Principer (manifesto)

- **Transparens**: Varje tool ska ha en läsbar spec; ingen "svart låda".
- **Öppenhet**: Datakällor och beroenden ska vara angivna och möjligtvis öppna.
