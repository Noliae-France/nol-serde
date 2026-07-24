# nol.serde

Sérialisation / désérialisation fiable en pur [Nolc](https://noliae-nolc.s3.gra.io.cloud.ovh.net/nolc-latest-linux-x86_64.tar.gz), sans dépendance lourde.

> **État : fondation (v0.1).** Les primitives ci-dessous sont implémentées et testées. La feuille de route liste la suite. Construit lot par lot, chaque étape avec CI verte.

## Installation

```toml
[dependances]
"nol-serde" = { git = "https://github.com/Noliae-France/nol-serde" }
```

## Licence

MIT © 2026 Bastien LANGUEDOC.

## Livré (v0.2)
Encodeur JSON **correct** : échappement complet des chaînes (`json_echappe` : `"`, `\\`, saut de ligne, retour chariot, tabulation) et composition de structures imbriquées.
- Scalaires : `json_null`, `json_bool`, `json_entier`, `json_chaine`, `json_brut`
- Composition : `json_tableau`, `json_objet`, `json_champ`, `json_tableau_chaines`
- Champs typés : `json_champ_chaine`, `json_champ_entier`, `json_champ_bool`

```nol
var champs: List<Text> = []
push(champs, json_champ_chaine("nom", "Alice"))
push(champs, json_champ_entier("age", 30))
json_objet(champs)   // => {"nom":"Alice","age":30}
```

## Feuille de route
- Décodage / parseur JSON typé
- **JSON Lines, MessagePack, TOML, YAML, CBOR**
