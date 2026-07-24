# nol.serde

Sérialisation / désérialisation fiable en pur [Nolc](https://github.com/Noliae-France/nolc), sans dépendance lourde.

> **État : fondation (v0.1).** Les primitives ci-dessous sont implémentées et testées. La feuille de route liste la suite. Construit lot par lot, chaque étape avec CI verte.

## Installation

```toml
[dependances]
"nol-serde" = { git = "https://github.com/Noliae-France/nol-serde" }
```

## Licence

MIT © 2026 Bastien LANGUEDOC.

## Livré (v0.1)
Encodage JSON des scalaires et listes (`json_bool`, `json_entier`, `json_chaine`, `json_liste_chaines`, `json_champ_chaine`).

## Feuille de route
- Échappement JSON complet + décodage typé
- **JSON Lines, MessagePack, TOML, YAML, CBOR**
