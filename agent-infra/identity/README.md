# Identity — OpenSverige Agent-Infrastruktur

Hur vi definierar **identitet** för våra agenter i OpenSverige.

## Syfte

Identity beskriver **vem** agenten är: namn, roller, gränser och vilka principer den representerar. Det gör agenten förutsägbar och ansvarig — användare ska veta att de pratar med en OpenSverige-agent som följer våra värderingar.

## Definition för OpenSverige

- **Format**: En tydlig identitetsfil (t.ex. `identity.md` eller strukturerad YAML/JSON) per agent eller agent-typ.
- **Placering**: `agent-infra/identity/` — alla agent-identiteter och roller samlas här.
- **Innehåll**:
  - **Namn och roll**: Vad agenten heter och vilken funktion den har (t.ex. "Support-agent", "Data-agent").
  - **Principer**: Referens till manifesto och eventuella policy-filer.
  - **Gränser**: Vad agenten **inte** får göra (t.ex. inte ge juridiskt råd, inte spara känslig data utan samtycke).
  - **Öppenhet**: Att identiteten är public och granskningsbar.

## Mall för en agent-identitet

```markdown
# [Agent-namn]

## Roll
En mening som beskriver agentens roll i OpenSverige.

## Principer
- Länk till [manifesto.md](../../manifesto.md)
- Eventuella tillägg: [länk]

## Gränser
- Agenten får inte: ...
- Agenten ska alltid: ...

## Version och ansvar
- Senast uppdaterad: YYYY-MM-DD
- Ansvarig/ägare: [team eller repo]
```

## Principer (manifesto)

- **Transparens**: Identiteten ska vara tydlig och public — ingen anonym eller dold agent.
- **Öppenhet**: Definition i repo så att alla kan se vilka roller och gränser som gäller.
