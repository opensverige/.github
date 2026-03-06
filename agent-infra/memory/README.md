# Memory — OpenSverige Agent-Infrastruktur

Hur vi definierar och hanterar **minne** för våra agenter i OpenSverige.

## Syfte

Memory beskriver vad agenten får komma ihåg över tid: användarpreferenser, konversationshistorik, domänfakta och policyer. Allt ska vara **genomskinligt** och **återanvändbart** — ingen hemlig eller ogenomskinlig state.

## Definition för OpenSverige

- **Format**: Strukturerad data (t.ex. JSON/JSONL eller tydliga Markdown-sektioner) som kan versioneras i repo.
- **Placering**: `agent-infra/memory/` — allt som rör långvarigt minne ligger här eller refererar hit.
- **Innehåll**:
  - **Användarkontext**: Vilka beslut/preferenser användaren gjort (sparade öppet, inte i hemliga caches).
  - **Fakta om domänen**: T.ex. vilka API:er, begrepp och regler som gäller för OpenSverige.
  - **Policyer**: Vilka regler agenten ska följa (länk till manifesto och specifika policy-filer).

## Mall för en memory-definition

```markdown
# [Namn på minneskontext]

## Beskrivning
Kort beskrivning av vad detta minne används till.

## Typ
- [ ] Användarkontext
- [ ] Domänfakta
- [ ] Policy

## Data (strukturerat)
<!-- JSON eller tydlig lista -->
```

## Principer (manifesto)

- **Transparens**: Minnesinnehåll ska kunna granskas och förstås av alla.
- **Öppenhet**: Definitioner i repo, inga enbart binära eller opåkallade caches.
