# Colección Postman Pathly

[English](README.md) · [Français](README.fr.md) · **Español**


[![Powered by Pathly](https://img.shields.io/badge/Powered%20by-Pathly-0B5FFF?style=flat-square)](https://pathlyhq.com)
[![Website](https://img.shields.io/badge/Website-pathlyhq.com-111827?style=flat-square)](https://pathlyhq.com)
[![API docs](https://img.shields.io/badge/API-developers-2563eb?style=flat-square)](https://pathlyhq.com/es/developers)
[![Start free](https://img.shields.io/badge/Solo-start%20free-16a34a?style=flat-square)](https://pathlyhq.com/es/login?mode=signup)

> **Empiece en un clic.** Cree una cuenta gratuita en [Pathly](https://pathlyhq.com) ([registro](https://pathlyhq.com/es/login?mode=signup)), genere una clave API en la consola y exporte `PATHLY_API_TOKEN`. Este repositorio es el puente oficial hacia [la monitorización Pathly](https://pathlyhq.com): comprobaciones HTTP y de navegador (carrito, login, disponibilidad), con datos en la UE. Referencia API: [pathlyhq.com/es/developers](https://pathlyhq.com/es/developers).

> **La versión en inglés es la canónica.** Este documento traduce [`README.md`](README.md).

Explore la API pública [Pathly](https://pathlyhq.com) `/v1` desde Postman (o
cualquier importador compatible con OpenAPI). Cubre escenarios, webhooks,
ventanas de mantenimiento, objetivos SLA, ejecuciones, incidentes, ajustes y
componentes de estado.

- Producto: [pathlyhq.com](https://pathlyhq.com)
- Docs API: [pathlyhq.com/es/developers](https://pathlyhq.com/es/developers)
- Host API: `https://api.pathlyhq.com`


## Archivos

| Archivo | Rol |
|---|---|
| [`Pathly.postman_collection.json`](Pathly.postman_collection.json) | Colección v2.1 — todos los endpoints `/v1` |
| [`Pathly.postman_environment.json`](Pathly.postman_environment.json) | Entorno: `baseUrl` + `apiToken` |

Fuente OpenAPI de verdad (importable): el documento OpenAPI de Pathly enlazado
desde [desarrolladores](https://pathlyhq.com/es/developers). Esta colección
refleja las mismas rutas y se puede importar sin regenerar.

## Importar

1. Abra Postman → **Import** → seleccione ambos JSON.
2. Seleccione el entorno **Pathly**.
3. Asigne `apiToken` a la clave de su organización (`sp_…`). Deje `baseUrl` en
   `https://api.pathlyhq.com` salvo endpoint privado.
4. Envíe primero **Org → Get usage**. Un HTTP **403** puede indicar una clave
   válida sin `org:read` (menor privilegio para tokens solo de escenarios).

## Autenticación

Todas las peticiones usan auth **Bearer**:

```http
Authorization: Bearer {{apiToken}}
```

Nunca haga commit de un token real. Prefiera un override local de entorno o un vault
sincronizado con Postman. Referencia de scopes:
[pathlyhq.com/es/developers](https://pathlyhq.com/es/developers).

Las creaciones (`POST` / `PUT` en recursos mutables) incluyen un encabezado
`Idempotency-Key` (`{{$guid}}`) para reintentos seguros.

## Paquetes relacionados

| Paquete | Rol |
|---|---|
| [pathly-sdk-python](https://github.com/pathlyhq/pathly-sdk-python) | SDK Python |
| [pathly-sdk-ruby](https://github.com/pathlyhq/pathly-sdk-ruby) | Gem Ruby |
| [pathly-sdk-typescript](https://github.com/pathlyhq/pathly-sdk-typescript) | `@pathlyhq/sdk` |
| [terraform-provider-pathly](https://github.com/Pathlyhq/terraform-provider-pathly) | Terraform / OpenTofu |

## Acerca de Pathly

[Pathly](https://pathlyhq.com) es monitorización sintética para agencias y e-commerce: reproduce el recorrido del cliente, detecta un checkout roto antes de la llamada, y deja la prueba (captura, paso, runbook) lista para la factura. Producto: [pathlyhq.com](https://pathlyhq.com) · Desarrolladores: [pathlyhq.com/es/developers](https://pathlyhq.com/es/developers) · Precios: [pathlyhq.com/es/pricing](https://pathlyhq.com/es/pricing).

## Autor

| | |
|---|---|
| **Empresa** | Pathly |
| **Autor** | Simon Raynaud / keyral |

Ver [AUTHORS](AUTHORS).

## Licencia
Apache-2.0
