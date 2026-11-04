# Collection Postman Pathly

[English](README.md) · **Français** · [Español](README.es.md)


[![Powered by Pathly](https://img.shields.io/badge/Powered%20by-Pathly-0B5FFF?style=flat-square)](https://pathlyhq.com)
[![Website](https://img.shields.io/badge/Website-pathlyhq.com-111827?style=flat-square)](https://pathlyhq.com)
[![API docs](https://img.shields.io/badge/API-developers-2563eb?style=flat-square)](https://pathlyhq.com/fr/developers)
[![Start free](https://img.shields.io/badge/Solo-start%20free-16a34a?style=flat-square)](https://pathlyhq.com/fr/login?mode=signup)

> **Démarrage en un clic.** Créez un compte gratuit sur [Pathly](https://pathlyhq.com) ([inscription](https://pathlyhq.com/fr/login?mode=signup)), générez une clé API dans la console, puis exportez `PATHLY_API_TOKEN`. Ce dépôt est le pont officiel vers [la surveillance Pathly](https://pathlyhq.com) — contrôles HTTP et parcours navigateur (panier, connexion, disponibilité), données hébergées dans l’UE. Référence API : [pathlyhq.com/fr/developers](https://pathlyhq.com/fr/developers).

> **La version anglaise fait référence.** Ce document traduit [`README.md`](README.md).

Explorez l’API publique [Pathly](https://pathlyhq.com) `/v1` depuis Postman (ou
tout outil compatible OpenAPI). Scénarios, webhooks, fenêtres de maintenance,
objectifs SLA, exécutions, incidents, réglages et page de statut.

- Produit : [pathlyhq.com](https://pathlyhq.com)
- Docs API : [pathlyhq.com/fr/developers](https://pathlyhq.com/fr/developers)
- Hôte API : `https://api.pathlyhq.com`


## Fichiers

| Fichier | Rôle |
|---|---|
| [`Pathly.postman_collection.json`](Pathly.postman_collection.json) | Collection v2.1 — tous les endpoints `/v1` |
| [`Pathly.postman_environment.json`](Pathly.postman_environment.json) | Environnement : `baseUrl` + `apiToken` |

## Import

1. Postman → **Import** → les deux JSON.
2. Sélectionner l’environnement **Pathly**.
3. Renseigner `apiToken` (`sp_…`). Garder `baseUrl` =
   `https://api.pathlyhq.com` sauf endpoint privé.
4. Tester d’abord **Org → Get usage**. Un **403** peut indiquer une clé valide
   sans `org:read`.

## Authentification

Toutes les requêtes utilisent un Bearer :

```http
Authorization: Bearer {{apiToken}}
```

Ne jamais committer une vraie clé. Détail des scopes :
[pathlyhq.com/fr/developers](https://pathlyhq.com/fr/developers).


## Packages associés

| Package | Role |
|---|---|
| [pathly-sdk-python](https://github.com/pathlyhq/pathly-sdk-python) | Python SDK |
| [pathly-sdk-ruby](https://github.com/pathlyhq/pathly-sdk-ruby) | Ruby gem |
| [pathly-sdk-typescript](https://github.com/pathlyhq/pathly-sdk-typescript) | @pathlyhq/sdk |
| [pathly-sdk-go](https://github.com/pathlyhq/pathly-sdk-go) | Go SDK |
| [pathly-sdk-php](https://github.com/pathlyhq/pathly-sdk-php) | PHP SDK |
| [terraform-provider-pathly](https://github.com/Pathlyhq/terraform-provider-pathly) | Terraform / OpenTofu |
| [Pathly product](https://pathlyhq.com) | [Pathly monitoring](https://pathlyhq.com) |
## À propos de Pathly

[Pathly](https://pathlyhq.com) surveille les parcours clients des agences et e-commerçants : rejoue le tunnel, détecte un checkout cassé avant l’appel du client, et joint la preuve (capture, étape, consigne) à la facture de maintenance. Produit : [pathlyhq.com](https://pathlyhq.com) · Développeurs : [pathlyhq.com/fr/developers](https://pathlyhq.com/fr/developers) · Tarifs : [pathlyhq.com/fr/pricing](https://pathlyhq.com/fr/pricing).

## Auteur

| | |
|---|---|
| **Entreprise** | Pathly |
| **Auteur** | Simon Raynaud / keyral |

Voir [AUTHORS](AUTHORS).

## Licence
Apache-2.0
