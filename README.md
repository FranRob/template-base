# template-base

Template de proyecto para Claude Code con setup multi-agente, memoria persistente via Engram y reglas modulares auto-cargadas.

## Qué incluye

```
.claude/
├── settings.json          # Hook post-compactación para recuperar estado de Engram
├── rules/
│   ├── git-workflow.md    # Gitflow + flujo de PRs (siempre activo)
│   └── security.md        # Baseline de seguridad (siempre activo)
└── agents/
    └── explorer.md        # Sub-agente que mapea el código sin editarlo

.engram/config.json        # Bloquea el nombre del proyecto para Engram
CLAUDE.md                  # Instrucciones del proyecto para Claude Code
CLAUDE.local.md.example    # Template para overrides personales (gitignoreado)
```

## Cómo usar este template

1. Hacé click en **Use this template** → Create a new repository
2. Cloná tu nuevo repo
3. Completá `CLAUDE.md` con los detalles de tu proyecto
4. Cambiá `project_name` en `.engram/config.json` por el nombre de tu repo
5. Copiá `CLAUDE.local.md.example` → `CLAUDE.local.md` y completá tus preferencias personales
6. Agregá reglas específicas de tu stack en `.claude/rules/`
7. Abrí Claude Code — todo está listo

## Qué personalizar

| Archivo | Qué hacer |
|---------|-----------|
| `CLAUDE.md` | Reemplazá los placeholders con la info de tu proyecto |
| `.engram/config.json` | Cambiá `CHANGE_ME` por el nombre de tu repo |
| `.claude/rules/` | Agregá reglas específicas de tu stack con frontmatter `paths:` |
| `.claude/agents/` | Agregá sub-agentes especializados que necesite tu proyecto |

## Sistema de reglas

Las reglas en `.claude/rules/` soportan frontmatter `paths:` — solo se cargan cuando Claude trabaja con archivos que coincidan. Esto mantiene el contexto liviano:

```markdown
---
description: Convenciones de API
paths:
  - "src/modules/**"
---
Tus reglas acá...
```

## Overrides personales

Copiá `CLAUDE.local.md.example` a `CLAUDE.local.md` (gitignoreado). Usalo para preferencias de idioma, quirks del entorno local o reglas de flujo de trabajo personales.
