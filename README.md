# metaltura/react

Le vocabulaire React, qui hérite de la partie « page unique » du métamodèle d'application. Le dépôt `node-react` le relie à Node.

## Ce qu'il contient

- `models/React.yaml` — le vocabulaire React (PLAT-308), qui hérite du paquet spa d'Application sans le changer : une interface React (Frontend) et son client d'API (ApiClient). Une interface React ne range que des clients d'API React : un service Angular y est signalé (`reactServicesOnly`).

## Ce dont il dépend

| Dépôt | Ce qu'il en emploie | Ligne `depends` |
| --- | --- | --- |
| `metaltura/application` | `Application`, que `React` désigne ou spécialise | `metaltura/application/Application@v1.0.0` |

`Diagram` et `Uml` sont des modèles système de Metaltura : leur nom seul suffit.

## L'utiliser depuis un autre dépôt

Écrire dans la liste `depends` du modèle :

```yaml
depends:
  - metaltura/react/React@v1.0.0
```

Metaltura clone ce dépôt à l'étiquette `v1.0.0`, puis `metaltura/application` dont il dépend, et `metaltura/domain` que ce dernier nomme. Toute la librairie est à `v1.0.0` : Metaltura refuse qu'un même dépôt soit demandé à deux versions.

## D'où il vient

Ce dépôt vient du dépôt privé `Kogitec/simple-mda`, `main` à `96a1a75` (PLAT-1461), rangé par sujet par PLAT-1498 en un seul commit : son modèle était sous `models/applications/node-react/`. L'historique de ses fichiers reste dans `simple-mda`, archivé.
