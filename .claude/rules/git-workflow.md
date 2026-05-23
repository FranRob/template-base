---
description: Estrategia de branches y flujo de PRs — siempre activo
---

## Estrategia de branches (Gitflow)

- `main` — solo producción. Se mergea desde `develop` en releases deliberados.
- `develop` — rama de integración. Todas las feature branches mergean acá.
- Feature branches — corta duración, una por bloque, se bifurcan desde `develop`, PR de vuelta a `develop`.

## Flujo de PRs (obligatorio)

Cada bloque de trabajo DEBE seguir este flujo — sin excepciones:

1. Crear un issue en GitHub describiendo el bloque → agregar label `status:approved`
2. Crear branch desde `develop`: `feat/bloque-XX-descripcion` (o `fix/`, `docs/`, etc.)
3. Trabajar con conventional commits
4. Abrir PR desde el branch → `develop`
5. Si el diff supera 400 líneas → dividir en stacked PRs
6. Mergear y cerrar el issue

Nunca acumular múltiples bloques en un solo PR.
